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
ms.openlocfilehash: 22d30e14256a2e58e05e17207380842392fe0c23
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887419"
---
# <a name="step-2-get-an-authentication-access-token"></a><span data-ttu-id="80f22-104">ขั้นตอนที่ 2: รับโทเค็นการเข้าถึงการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="80f22-104">Step 2: Get an authentication access token</span></span>

<span data-ttu-id="80f22-105">บทความนี้คือ ขั้นตอนที่สองในชุด[พุชข้อมูลลงในชุดข้อมูล Power BI](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="80f22-105">This article is the second step in the series [Push data into a Power BI dataset](walkthrough-push-data.md).</span></span>

<span data-ttu-id="80f22-106">ในขั้นตอนที่ 1 คุณ[ได้ลงทะเบียนแอปไคลเอ็นต์ใน Azure AD แล้ว](../embedded/register-app.md)</span><span class="sxs-lookup"><span data-stu-id="80f22-106">In step 1, you [registered a client app in Azure AD](../embedded/register-app.md).</span></span> <span data-ttu-id="80f22-107">ในขั้นตอนนี้ คุณจะได้รับโทเค็นการเข้าถึงการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="80f22-107">In this step, you get an authentication access token.</span></span> <span data-ttu-id="80f22-108">แอป Power BI จะรวมกับ Azure AD Directory เพื่อให้สามารถเข้าสู่ระบบได้อย่างปลอดภัยรวมถึงการตรวจสอบสำหรับแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="80f22-108">Power BI apps are integrated with Azure Active Directory to provide your app with secure sign in and authorization.</span></span> <span data-ttu-id="80f22-109">แอปของคุณใช้โทเค็นเพื่อรับรองความถูกต้องในการเข้าถึง Azure AD และเพื่อเข้าถึงแหล่งข้อมูลของ Power BI</span><span class="sxs-lookup"><span data-stu-id="80f22-109">Your app uses a token to authenticate to Azure AD and gain access to Power BI resources.</span></span>

## <a name="get-an-authentication-access-token"></a><span data-ttu-id="80f22-110">รับโทเค็นการเข้าใช้การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="80f22-110">Get an authentication access token</span></span>

<span data-ttu-id="80f22-111">ก่อนที่จะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้เสร็จสิ้น[ขั้นตอนก่อนหน้า](../embedded/register-app.md)ในการ[พุชข้อมูลลงในชุดของชุดข้อมูล Power BI](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="80f22-111">Before starting, make sure you've completed the [previous step](../embedded/register-app.md) in the [Push data into a Power BI dataset](walkthrough-push-data.md) series.</span></span> 

<span data-ttu-id="80f22-112">ขั้นตอนนี้จำเป็นต้องใช้ Visual Studio 2015 ขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="80f22-112">This procedure requires Visual Studio 2015 or later.</span></span>

1. <span data-ttu-id="80f22-113">สร้างโครงการ **แอปพลิเคชันคอนโซล** C# ใหม่ใน Studio Visual 2015</span><span class="sxs-lookup"><span data-stu-id="80f22-113">In Visual Studio, create a new C# **Console Application** project.</span></span>

2. <span data-ttu-id="80f22-114">ติดตั้ง[ไลบรารีรับรองความถูกต้อง AD Azure สำหรับแพคเกจ .NET NuGet](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/2.22.302111727)</span><span class="sxs-lookup"><span data-stu-id="80f22-114">Install the [Azure AD Authentication Library for .NET NuGet package](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/2.22.302111727).</span></span> <span data-ttu-id="80f22-115">แอป .Net ของคุณต้องการแพคเกจนี้เพื่อรับโทเค็นรักษาความปลอดภัยการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="80f22-115">Your .Net app needs this package to get an authentication security token.</span></span> 

     <span data-ttu-id="80f22-116">a.</span><span class="sxs-lookup"><span data-stu-id="80f22-116">a.</span></span> <span data-ttu-id="80f22-117">เลือก **เครื่องมือ** > **ตัวจัดการแพคเกจ NuGet** > **คอนโซลตัวจัดการแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="80f22-117">Select **Tools** > **NuGet Package Manager** > **Package Manager Console**.</span></span>

     <span data-ttu-id="80f22-118">b.</span><span class="sxs-lookup"><span data-stu-id="80f22-118">b.</span></span> <span data-ttu-id="80f22-119">ป้อน **Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612**</span><span class="sxs-lookup"><span data-stu-id="80f22-119">Enter **Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612**</span></span>

     <span data-ttu-id="80f22-120">c.</span><span class="sxs-lookup"><span data-stu-id="80f22-120">c.</span></span> <span data-ttu-id="80f22-121">ใน Program.cs เพิ่ม`using Microsoft.IdentityModel.Clients.ActiveDirectory;`</span><span class="sxs-lookup"><span data-stu-id="80f22-121">In Program.cs, add `using Microsoft.IdentityModel.Clients.ActiveDirectory;`.</span></span>

3. <span data-ttu-id="80f22-122">เพิ่มตัวอย่างรหัสที่แสดงขึ้นหลังจากขั้นตอนเหล่านี้ลงใน Program.cs</span><span class="sxs-lookup"><span data-stu-id="80f22-122">Add the sample code listed after these steps to Program.cs.</span></span>

4. <span data-ttu-id="80f22-123">แทนที่ "{ClientID }" ด้วย **ไคลเอ็นต์ ID** ที่คุณได้ใน [บทความชุดก่อนหน้า](../embedded/register-app.md)เมื่อคุณลงทะเบียนแอปของคุณ</span><span class="sxs-lookup"><span data-stu-id="80f22-123">Replace "{ClientID}", with the **Client ID** you got in the [previous series article](../embedded/register-app.md) when you registered your app.</span></span>

5. <span data-ttu-id="80f22-124">เรียกใช้แอปคอนโซล และลงชื่อเข้าใช้บัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="80f22-124">Run your console app and sign in to your Power BI account.</span></span> 

   <span data-ttu-id="80f22-125">สตริงโทเค็นควรปรากฏในหน้าต่างคอนโซล</span><span class="sxs-lookup"><span data-stu-id="80f22-125">A token string should appear in the console window.</span></span>

<span data-ttu-id="80f22-126">**ตัวอย่างรหัสเพื่อรับโทเค็นรักษาความปลอดภัยการรับรองความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="80f22-126">**Sample code to get authentication security token**</span></span>

<span data-ttu-id="80f22-127">เพิ่มรหัสนี้ลงในโปรแกรม {...}</span><span class="sxs-lookup"><span data-stu-id="80f22-127">Add this code to Program {...}.</span></span>

* <span data-ttu-id="80f22-128">ตัวแปรโทเค็นสำหรับเรียกใช้การดำเนินการ:</span><span class="sxs-lookup"><span data-stu-id="80f22-128">A token variable to call operations:</span></span> 
  
  ```csharp
  private static string token = string.Empty;
  
  static void Main(string[] args)
  {
  }
  ```
* <span data-ttu-id="80f22-129">ใน static void Main(string[] args):</span><span class="sxs-lookup"><span data-stu-id="80f22-129">In static void Main(string[] args):</span></span>
  
  ```csharp
  static void Main(string[] args)
  {
    //Get an authentication access token
    token = GetToken();
  }
  ```
* <span data-ttu-id="80f22-130">เพิ่มวิธีการ GetToken():</span><span class="sxs-lookup"><span data-stu-id="80f22-130">Add a GetToken() method:</span></span>

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
           string authorityUri = "https://login.microsoftonline.net/common/";

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

<span data-ttu-id="80f22-131">หลังจากที่คุณได้รับโทเค็นรับรองความถูกต้อง คุณสามารถเรียกการดำเนินการ Power BI ต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="80f22-131">After you get an authentication token, you can call any Power BI operation.</span></span>

<span data-ttu-id="80f22-132">บทความถัดไปในชุดนี้แสดงถึงวิธีการ[สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)</span><span class="sxs-lookup"><span data-stu-id="80f22-132">The next article in this series shows you how to [Create a dataset in Power BI](walkthrough-push-data-create-dataset.md).</span></span>


## <a name="complete-code-listing"></a><span data-ttu-id="80f22-133">รายการรหัสเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="80f22-133">Complete code listing</span></span>

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



## <a name="next-steps"></a><span data-ttu-id="80f22-134">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="80f22-134">Next steps</span></span>

* <span data-ttu-id="80f22-135">บทความถัดไปในชุดนี้คือ[สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)</span><span class="sxs-lookup"><span data-stu-id="80f22-135">The next article in this series is [Create a dataset in Power BI](walkthrough-push-data-create-dataset.md)</span></span>
* [<span data-ttu-id="80f22-136">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="80f22-136">Overview of Power BI REST API</span></span>](overview-of-power-bi-rest-api.md)  
* [<span data-ttu-id="80f22-137">Power BI REST APIs</span><span class="sxs-lookup"><span data-stu-id="80f22-137">Power BI REST APIs</span></span>](/rest/api/power-bi/)  

<span data-ttu-id="80f22-138">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="80f22-138">More questions?</span></span> [<span data-ttu-id="80f22-139">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="80f22-139">Try the Power BI Community</span></span>](https://community.powerbi.com/)