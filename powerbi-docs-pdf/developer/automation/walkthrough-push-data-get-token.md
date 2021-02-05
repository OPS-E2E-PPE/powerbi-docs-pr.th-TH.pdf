---
title: รับโทเค็นการเข้าใช้การรับรองความถูกต้องในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: คำแนะนำการส่งข้อมูล - รับโทเค็นการเข้าถึงการรับรองความถูกต้อง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.date: 05/29/2019
ms.openlocfilehash: 8959a0ac63ff1f182bcb3544b1925529b1ad3663
ms.sourcegitcommit: 2e81649476d5cb97701f779267be59e393460097
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "99422409"
---
# <a name="step-2-get-an-authentication-access-token"></a>ขั้นตอนที่ 2: รับโทเค็นการเข้าถึงการรับรองความถูกต้อง

บทความนี้คือ ขั้นตอนที่สองในชุด[พุชข้อมูลลงในชุดข้อมูล Power BI](walkthrough-push-data.md)

ในขั้นตอนที่ 1 คุณ[ได้ลงทะเบียนแอปไคลเอ็นต์ใน Azure AD แล้ว](../embedded/register-app.md) ในขั้นตอนนี้ คุณจะได้รับโทเค็นการเข้าถึงการรับรองความถูกต้อง แอป Power BI จะรวมกับ Azure AD Directory เพื่อให้สามารถเข้าสู่ระบบได้อย่างปลอดภัยรวมถึงการตรวจสอบสำหรับแอปของคุณ แอปของคุณใช้โทเค็นเพื่อรับรองความถูกต้องในการเข้าถึง Azure AD และเพื่อเข้าถึงแหล่งข้อมูลของ Power BI

## <a name="get-an-authentication-access-token"></a>รับโทเค็นการเข้าใช้การรับรองความถูกต้อง

ก่อนที่จะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้เสร็จสิ้น[ขั้นตอนก่อนหน้า](../embedded/register-app.md)ในการ[พุชข้อมูลลงในชุดของชุดข้อมูล Power BI](walkthrough-push-data.md) 

ขั้นตอนนี้จำเป็นต้องใช้ Visual Studio 2015 ขึ้นไป

1. สร้างโครงการ **แอปพลิเคชันคอนโซล** C# ใหม่ใน Studio Visual 2015

2. ติดตั้ง[ไลบรารีรับรองความถูกต้อง AD Azure สำหรับแพคเกจ .NET NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/2.22.302111727) แอป .Net ของคุณต้องการแพคเกจนี้เพื่อรับโทเค็นรักษาความปลอดภัยการรับรองความถูกต้อง 

     a. เลือก **เครื่องมือ** > **ตัวจัดการแพคเกจ NuGet** > **คอนโซลตัวจัดการแพคเกจ**

     b. ป้อน **Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612**

     c. ใน Program.cs เพิ่ม`using Microsoft.IdentityModel.Clients.ActiveDirectory;`

3. เพิ่มตัวอย่างรหัสที่แสดงขึ้นหลังจากขั้นตอนเหล่านี้ลงใน Program.cs

4. แทนที่ "{ClientID }" ด้วย **ไคลเอ็นต์ ID** ที่คุณได้ใน [บทความชุดก่อนหน้า](../embedded/register-app.md)เมื่อคุณลงทะเบียนแอปของคุณ

5. เรียกใช้แอปคอนโซล และลงชื่อเข้าใช้บัญชี Power BI ของคุณ 

   สตริงโทเค็นควรปรากฏในหน้าต่างคอนโซล

**ตัวอย่างรหัสเพื่อรับโทเค็นรักษาความปลอดภัยการรับรองความถูกต้อง**

เพิ่มรหัสนี้ลงในโปรแกรม {...}

* ตัวแปรโทเค็นสำหรับเรียกใช้การดำเนินการ: 
  
  ```csharp
  private static string token = string.Empty;
  
  static void Main(string[] args)
  {
  }
  ```
* ใน static void Main(string[] args):
  
  ```csharp
  static void Main(string[] args)
  {
    //Get an authentication access token
    token = GetToken();
  }
  ```
* เพิ่มวิธีการ GetToken():

```csharp
       #region Get an authentication access token
       private static async Task<string> GetToken()
       {
           // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
           // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

           //The client id that Azure AD created when you registered your client app.
           string clientID = "{Client_ID}";

           //RedirectUri you used when you register your app.
           //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
           // You can use this redirect uri for your client app
           string redirectUri = "https://login.live.com/oauth20_desktop.srf";

           //Resource Uri for Power BI API
           string resourceUri = "https://analysis.windows.net/powerbi/api";

           //OAuth2 authority Uri
           string authorityUri = "https://login.microsoftonline.com/common/";

           //Get access token:
           // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
           // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
           // To install the Active Directory Authentication Library NuGet package in Visual Studio,
           //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

           // AcquireToken will acquire an Azure access token
           // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
           AuthenticationContext authContext = new AuthenticationContext(authorityUri);
           var token = authContext.AcquireTokenAsync(resourceUri, clientID, new Uri(redirectUri)).Result.AccessToken;

           Console.WriteLine(token);
           Console.ReadLine();

           return token;
       }

       #endregion
```

หลังจากที่คุณได้รับโทเค็นรับรองความถูกต้อง คุณสามารถเรียกการดำเนินการ Power BI ต่างๆได้

บทความถัดไปในชุดนี้แสดงถึงวิธีการ[สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)


## <a name="complete-code-listing"></a>รายการรหัสเสร็จสมบูรณ์

```csharp
using System;
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace walkthrough_push_data
{
    class Program
    {
        private static string token = string.Empty;

        static void Main(string[] args)
        {

            //Get an authentication access token
            token = GetToken();

        }

        #region Get an authentication access token
        private static async Task<string> GetToken()
        {
            // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
            // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

            //The client id that Azure AD created when you registered your client app.
            string clientID = "{Client_ID}";

            //RedirectUri you used when you register your app.
            //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
            // You can use this redirect uri for your client app
            string redirectUri = "https://login.live.com/oauth20_desktop.srf";

            //Resource Uri for Power BI API
            string resourceUri = "https://analysis.windows.net/powerbi/api";

            //OAuth2 authority Uri
            string authorityUri = "https://login.microsoftonline.com/common/";

            //Get access token:
            // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
            // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
            // To install the Active Directory Authentication Library NuGet package in Visual Studio,
            //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

            // AcquireToken will acquire an Azure access token
            // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
            AuthenticationContext authContext = new AuthenticationContext(authorityUri);
            var token = authContext.AcquireTokenAsync(resourceUri, clientID, new Uri(redirectUri)).Result.AccessToken;

            Console.WriteLine(token);
            Console.ReadLine();

            return token;
        }

        #endregion

    }
}
```



## <a name="next-steps"></a>ขั้นตอนถัดไป

* บทความถัดไปในชุดนี้คือ[สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)
* [ภาพรวมของ Power BI REST API](overview-of-power-bi-rest-api.md)  
* [Power BI REST APIs](/rest/api/power-bi/)  

มีคำถามเพิ่มเติมหรือไม่ [ลองไปที่ชุมชน Power BI](https://community.powerbi.com/)