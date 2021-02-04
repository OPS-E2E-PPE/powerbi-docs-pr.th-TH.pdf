---
title: รับรองความถูกต้องผู้ใช้และรับโทเค็นการเข้าถึง Azure AD สำหรับแอปพลิเคชันการวิเคราะห์แบบฝัง Power BI ของคุณเพื่อปรับปรุงประสบการณ์ BI แบบฝังตัวของลูกค้า
description: เรียนรู้วิธีการลงทะเบียนแอปพลิเคชันใน Azure Active Directory สำหรับการใช้งานด้วยการฝังเนื้อหา Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 06/04/2019
ms.openlocfilehash: 8001dd0e15ef713fa67256a45f645b0d7a0890c0
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888454"
---
# <a name="get-an-azure-ad-access-token-for-your-power-bi-application"></a><span data-ttu-id="7f41a-104">รับโทเค็นการเข้าถึง Azure AD สำหรับแอปพลิเคชัน Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f41a-104">Get an Azure AD access token for your Power BI application</span></span>

<span data-ttu-id="7f41a-105">บทความนี้แสดงวิธีที่คุณสามารถรับรองความถูกต้องผู้ใช้ในแอปพลิเคชัน Power BI ของคุณ และค้นคืนโทเค็นการเข้าถึงเพื่อใช้กับ [Power BI REST API](/rest/api/power-bi/)</span><span class="sxs-lookup"><span data-stu-id="7f41a-105">This article shows how you can authenticate users in your Power BI application and retrieve an access token to use with the [Power BI REST API](/rest/api/power-bi/).</span></span>

<span data-ttu-id="7f41a-106">ก่อนที่คุณจะสามารถเรียกใช้ REST API คุณจำเป็นต้องรับ Azure Active Directory (Azure AD) **โทเค็นการเข้าถึงการรับรองความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="7f41a-106">Before your app calls the REST API, you need to get an Azure Active Directory (Azure AD) **authentication access token**.</span></span> <span data-ttu-id="7f41a-107">แอปของคุณใช้โทเค็นเพื่อเข้าถึงยังแดชบอร์ด ไทล์ และรายงาน Power BI</span><span class="sxs-lookup"><span data-stu-id="7f41a-107">Your app uses a token to get access to Power BI dashboards, tiles, and reports.</span></span> <span data-ttu-id="7f41a-108">เมื่อต้องการเรียนรู้เพิ่มเติม ดู[ให้สิทธิอนุญาตการเข้าถึง Azure Active Directory โดยใช้โฟลว์ที่อนุญาตให้ใช้รหัส OAuth 2.0](/azure/active-directory/develop/v1-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="7f41a-108">To learn more, see [Authorize access to Azure Active Directory web applications using the OAuth 2.0 code grant flow](/azure/active-directory/develop/v1-protocols-oauth-code).</span></span>

<span data-ttu-id="7f41a-109">โทเค็นการเข้าถึงจะถูกเรียกใช้แตกต่างกัน ขึ้นอยู่กับวิธีการที่คุณจะฝังเนื้อหา </span><span class="sxs-lookup"><span data-stu-id="7f41a-109">Depending on how you're embedding content, the access token is retrieved differently.</span></span> <span data-ttu-id="7f41a-110">บทความนี้แสดงถึงสองวิธีการที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7f41a-110">This article shows two different approaches.</span></span>

## <a name="access-token-for-power-bi-users-user-owns-data"></a><span data-ttu-id="7f41a-111">โทเค็นการเข้าถึงสำหรับผู้ใช้ Power BI (ผู้ใช้เป็นเจ้าของข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="7f41a-111">Access token for Power BI users (user owns data)</span></span>

<span data-ttu-id="7f41a-112">ตัวอย่างนี้สำหรับเมื่อผู้ใช้ของคุณลงชื่อเข้าใช้ Azure AD ด้วยตนเองโดยเข้าสู่ระบบขององค์กร</span><span class="sxs-lookup"><span data-stu-id="7f41a-112">This example is for when your users manually sign into Azure AD with their organization sign in.</span></span> <span data-ttu-id="7f41a-113">จะมีการใช้งานนี้เมื่อมีการฝังเนื้อหาสำหรับผู้ใช้ที่มีสิทธิการเข้าถึงบริการ Power BI</span><span class="sxs-lookup"><span data-stu-id="7f41a-113">This task is used when embedding content for users that have Power BI service access.</span></span>

### <a name="get-an-azure-ad-authorization-code"></a><span data-ttu-id="7f41a-114">รับรหัสการให้สิทธิจาก Azure AD</span><span class="sxs-lookup"><span data-stu-id="7f41a-114">Get an Azure AD authorization code</span></span>

<span data-ttu-id="7f41a-115">ขั้นตอนแรกในการรับ **โทเค็นการเข้าถึง** คือการรับรหัสการให้สิทธิ์จาก **Azure AD**</span><span class="sxs-lookup"><span data-stu-id="7f41a-115">The first step to get an **access token** is to get an authorization code from **Azure AD**.</span></span> <span data-ttu-id="7f41a-116">คุณจะต้องสร้างสตริงแบบสอบถามกับคุณสมบัติต่อไปนี้ และเปลี่ยนเส้นทางไปยัง **Azure AD**</span><span class="sxs-lookup"><span data-stu-id="7f41a-116">Construct a query string with the following properties, and redirect to **Azure AD**.</span></span>

#### <a name="authorization-code-query-string"></a><span data-ttu-id="7f41a-117">สตริงแบบสอบถามรหัสการให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="7f41a-117">Authorization code query string</span></span>

```csharp
var @params = new NameValueCollection
{
    //Azure AD will return an authorization code. 
    //See the Redirect class to see how "code" is used to AcquireTokenByAuthorizationCode
    {"response_type", "code"},

    //Client ID is used by the application to identify themselves to the users that they are requesting permissions from.
    //You get the client id when you register your Azure app.
    {"client_id", Properties.Settings.Default.ClientID},

    //Resource uri to the Power BI resource to be authorized
    // https://analysis.windows.net/powerbi/api
    {"resource", Properties.Settings.Default.PowerBiAPI},

    //After user authenticates, Azure AD will redirect back to the web app
    {"redirect_uri", "https://localhost:13526/Redirect"}
};
```

<span data-ttu-id="7f41a-118">หลังจากที่คุณสร้างสตริงแบบสอบถามแล้ว เปลี่ยนเส้นทางไปยัง **Azure AD** เพื่อรับ **รหัสการให้สิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="7f41a-118">After you construct a query string, you redirect to **Azure AD** to get an **authorization code**.</span></span>  <span data-ttu-id="7f41a-119">ด้านล่างนี้คือวิธีการ์ C# ที่สมบูรณที่จะสร้าง **รหัสการตรวจสอบ** สตริงค้นหา และเปลี่ยนเส้นทางไปยัง **Azure AD**</span><span class="sxs-lookup"><span data-stu-id="7f41a-119">Below is a complete C# method to construct an **authorization code** query string, and redirect to **Azure AD**.</span></span> <span data-ttu-id="7f41a-120">จากนั้นคุณใช้ **รหัสการให้สิทธิ** เพื่อรับ **โทเค็นการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="7f41a-120">You then use the **authorization code** to get an **access token**.</span></span>

<span data-ttu-id="7f41a-121">ภายใน redirect.aspx.cs, จะเรียก [AuthenticationContext.AcquireTokenByAuthorizationCode](/dotnet/api/microsoft.identitymodel.clients.activedirectory.authenticationcontext.acquiretokenbyauthorizationcodeasync#Microsoft_IdentityModel_Clients_ActiveDirectory_AuthenticationContext_AcquireTokenByAuthorizationCodeAsync_System_String_System_Uri_Microsoft_IdentityModel_Clients_ActiveDirectory_ClientCredential_System_String_) เพื่อสร้างโทเค็น</span><span class="sxs-lookup"><span data-stu-id="7f41a-121">Within redirect.aspx.cs, [AuthenticationContext.AcquireTokenByAuthorizationCode](/dotnet/api/microsoft.identitymodel.clients.activedirectory.authenticationcontext.acquiretokenbyauthorizationcodeasync#Microsoft_IdentityModel_Clients_ActiveDirectory_AuthenticationContext_AcquireTokenByAuthorizationCodeAsync_System_String_System_Uri_Microsoft_IdentityModel_Clients_ActiveDirectory_ClientCredential_System_String_) calls to generate the token.</span></span>

#### <a name="get-authorization-code"></a><span data-ttu-id="7f41a-122">รับรหัสการให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="7f41a-122">Get authorization code</span></span>

```csharp
protected void signInButton_Click(object sender, EventArgs e)
{
    //Create a query string
    //Create a sign-in NameValueCollection for query string
    var @params = new NameValueCollection
    {
        //Azure AD will return an authorization code. 
        //See the Redirect class to see how "code" is used to AcquireTokenByAuthorizationCode
        {"response_type", "code"},

        //Client ID is used by the application to identify themselves to the users that they are requesting permissions from. 
        //You get the client id when you register your Azure app.
        {"client_id", Properties.Settings.Default.ClientID},

        //Resource uri to the Power BI resource to be authorized
        // https://analysis.windows.net/powerbi/api
        {"resource", Properties.Settings.Default.PowerBiAPI},

        //After user authenticates, Azure AD will redirect back to the web app
        {"redirect_uri", "https://localhost:13526/Redirect"}
    };

    //Create sign-in query string
    var queryString = HttpUtility.ParseQueryString(string.Empty);
    queryString.Add(@params);

    //Redirect authority
    //Authority Uri is an Azure resource that takes a client id to get an Access token
    // AADAuthorityUri = https://login.microsoftonline.com/common/
    string authorityUri = Properties.Settings.Default.AADAuthorityUri;
    var authUri = String.Format("{0}?{1}", authorityUri, queryString);
    Response.Redirect(authUri);
}
```

### <a name="get-an-access-token-from-authorization-code"></a><span data-ttu-id="7f41a-123">รับโทเค็นการเข้าถึงจากรหัสการให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="7f41a-123">Get an access token from authorization code</span></span>

<span data-ttu-id="7f41a-124">เมื่อ **Azure AD** เปลี่ยนเส้นทางกลับไปยังเว็บแอปของคุณด้วย **รหัสการให้สิทธิ** คุณสามารถใช้รหัสการให้สิทธิเพื่อรับโทเค็นการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="7f41a-124">Once **Azure AD** redirects back to your web app with an **authorization code**, you can use it to get an access token.</span></span> <span data-ttu-id="7f41a-125">ด้านล่างนี้คือ ตัวอย่าง C# ที่คุณสามารถใช้ในหน้าการเปลี่ยนเส้นทางของคุณกลับไปยังหน้าและเหตุการณ์ `Page_Load`ของ default.aspx ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7f41a-125">Below is a C# sample that you can use in your redirect page and the default.aspx's `Page_Load` event.</span></span>

<span data-ttu-id="7f41a-126">คุณสามารถค้นคืนเนมสเปซ **Microsoft.IdentityModel.Clients.ActiveDirectory** จาก [ไลบรารีการรับรองความถูกต้อง Active Directory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) แพคเกจ NuGetได้</span><span class="sxs-lookup"><span data-stu-id="7f41a-126">You can retrieve the **Microsoft.IdentityModel.Clients.ActiveDirectory** namespace from the [Active Directory Authentication Library](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) NuGet package.</span></span>

```powershell
Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory
```

#### <a name="redirectaspxcs"></a><span data-ttu-id="7f41a-127">Redirect.aspx.cs</span><span class="sxs-lookup"><span data-stu-id="7f41a-127">Redirect.aspx.cs</span></span>

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;

protected void Page_Load(object sender, EventArgs e)
{
    //Redirect uri must match the redirect_uri used when requesting Authorization code.
    string redirectUri = String.Format("{0}Redirect", Properties.Settings.Default.RedirectUrl);
    string authorityUri = Properties.Settings.Default.AADAuthorityUri;

    // Get the auth code
    string code = Request.Params.GetValues(0)[0];

    // Get auth token from auth code
    TokenCache TC = new TokenCache();

    AuthenticationContext AC = new AuthenticationContext(authorityUri, TC);
    ClientCredential cc = new ClientCredential
        (Properties.Settings.Default.ClientID,
        Properties.Settings.Default.ClientSecret);

    AuthenticationResult AR = AC.AcquireTokenByAuthorizationCode(code, new Uri(redirectUri), cc);

    //Set Session "authResult" index string to the AuthenticationResult
    Session[_Default.authResultString] = AR;

    //Redirect back to Default.aspx
    Response.Redirect("/Default.aspx");
}
```

#### <a name="defaultaspx"></a><span data-ttu-id="7f41a-128">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="7f41a-128">Default.aspx</span></span>

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;

protected void Page_Load(object sender, EventArgs e)
{

    //Test for AuthenticationResult
    if (Session[authResultString] != null)
    {
        //Get the authentication result from the session
        authResult = (AuthenticationResult)Session[authResultString];

        //Show Power BI Panel
        signInStatus.Visible = true;
        signInButton.Visible = false;

        //Set user and token from authentication result
        userLabel.Text = authResult.UserInfo.DisplayableId;
        accessTokenTextbox.Text = authResult.AccessToken;
    }
}
```

## <a name="access-token-for-non-power-bi-users-app-owns-data"></a><span data-ttu-id="7f41a-129">โทเค็นการเข้าถึงสำหรับผู้ใช้ที่ไม่ใช่ Power BI (แอปเป็นเจ้าของข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="7f41a-129">Access token for non-Power BI users (app owns data)</span></span>

<span data-ttu-id="7f41a-130">โดยทั่วไปวิธีการนี้จะใช้สำหรับแอปพลิเคชันจากบริษัทพัฒนาซอฟแวร์อิสระ (ISV) ที่แอปเป็นเจ้าของการเข้าถึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7f41a-130">This approach is typically used for independent software vendor (ISV) type applications where the app owns access to the data.</span></span> <span data-ttu-id="7f41a-131">ผู้ใช้ไม่จำเป็นต้องเป็นผู้ใช้ Power BI และการรับรองความถูกต้องผู้ใช้ของตัวควบคุมแอปพลิเคชัน และการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="7f41a-131">Users aren't necessarily Power BI users, and the application controls user authentication and access.</span></span>

### <a name="access-token-with-a-master-account"></a><span data-ttu-id="7f41a-132">โทเค็นการเข้าถึงด้วยบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="7f41a-132">Access token with a master account</span></span>

<span data-ttu-id="7f41a-133">สำหรับวิธีการนี้ คุณจะใช้บัญชี *หลัก* เดี่ยวที่เป็นผู้ใช้ Power BI Pro</span><span class="sxs-lookup"><span data-stu-id="7f41a-133">For this approach, you use a single *master* account that is a Power BI Pro user.</span></span> <span data-ttu-id="7f41a-134">ข้อมูลประจำตัวของบัญชีนี้ถูกเก็บไว้กับแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7f41a-134">The account credentials are stored with the application.</span></span> <span data-ttu-id="7f41a-135">แอปพลิเคชันจะรับรองความถูกต้องกับ Azure AD ด้วยข้อมูลประจำตัวที่จัดเก็บไว้เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7f41a-135">The application authenticates against Azure AD with these stored credentials.</span></span> <span data-ttu-id="7f41a-136">รหัสตัวอย่างที่แสดงด้านล่างนี้มาจาก[แอปที่เป็นเจ้าของตัวอย่างข้อมูล](https://github.com/guyinacube/PowerBI-Developer-Samples)</span><span class="sxs-lookup"><span data-stu-id="7f41a-136">The example code shown below comes from the [App owns data sample](https://github.com/guyinacube/PowerBI-Developer-Samples)</span></span>

### <a name="access-token-with-service-principal"></a><span data-ttu-id="7f41a-137">โทเค็นการเข้าถึงด้วยบริการหลัก</span><span class="sxs-lookup"><span data-stu-id="7f41a-137">Access token with service principal</span></span>

<span data-ttu-id="7f41a-138">สำหรับวิธีนี้ คุณใช้ [บริการหลัก](embed-service-principal.md)ซึ่งก็คือ **โทเค็นเฉพาะแอป**</span><span class="sxs-lookup"><span data-stu-id="7f41a-138">For this approach, you use a [service principal](embed-service-principal.md), that is an **app-only** token.</span></span> <span data-ttu-id="7f41a-139">แอปพลิเคชันจะรับรองความถูกต้องกับ Azure AD ด้วยบริการหลัก</span><span class="sxs-lookup"><span data-stu-id="7f41a-139">The application authenticates against Azure AD with service principal.</span></span> <span data-ttu-id="7f41a-140">รหัสตัวอย่างที่แสดงด้านล่างนี้มาจาก[แอปที่เป็นเจ้าของตัวอย่างข้อมูล](https://github.com/guyinacube/PowerBI-Developer-Samples)</span><span class="sxs-lookup"><span data-stu-id="7f41a-140">The example code shown below comes from the [App owns data sample](https://github.com/guyinacube/PowerBI-Developer-Samples)</span></span>

#### <a name="embedservicecs"></a><span data-ttu-id="7f41a-141">EmbedService.cs</span><span class="sxs-lookup"><span data-stu-id="7f41a-141">EmbedService.cs</span></span>

```csharp
var AuthorityURL  = "https://login.microsoftonline.com/<TenantId>/"
var ResourceURL  = "https://analysis.windows.net/powerbi/api"
var authenticationContext = new AuthenticationContext(AuthorityUrl);
       AuthenticationResult authenticationResult = null;
       if (AuthenticationType.Equals("MasterUser"))
       {
              // Authentication using master user credentials
              var credential = new UserPasswordCredential(Username, Password);
              authenticationResult = authenticationContext.AcquireTokenAsync(ResourceUrl, ApplicationId, credential).Result;
       }
       else
       {
             // Authentication using app credentials
             var credential = new ClientCredential(ApplicationId, ApplicationSecret);
             authenticationResult = await authenticationContext.AcquireTokenAsync(ResourceUrl, credential);
       }


m_tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");
```

## <a name="troubleshoot"></a><span data-ttu-id="7f41a-142">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="7f41a-142">Troubleshoot</span></span>

<span data-ttu-id="7f41a-143">ข้อความแสดงข้อผิดพลาด "'AuthenticationContext' ไม่มีคำจำกัดความของ 'AcquireToken' และไม่พบการเข้าถึง 'AcquireToken' ที่ยอมรับอาร์กิวเมนต์แรกในประเภท 'AuthenticationContext' (คุณไม่ได้ใช้คำสั่งหรือการอ้างอิงแอสเซมบลีใช่หรือไม่)"</span><span class="sxs-lookup"><span data-stu-id="7f41a-143">Error message: "'AuthenticationContext' doesn't contain a definition for 'AcquireToken' and no accessible 'AcquireToken' accepting a first argument of type 'AuthenticationContext' could be found (are you missing a using directive or an assembly reference?)".</span></span>

   <span data-ttu-id="7f41a-144">ลองดาวน์โหลด[Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/2.22.302111727)ถ้าคุณเห็นข้อผิดพลาดนี้</span><span class="sxs-lookup"><span data-stu-id="7f41a-144">Try downloading [Microsoft.IdentityModel.Clients.ActiveDirectory](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/2.22.302111727) if you see this error.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7f41a-145">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="7f41a-145">Next steps</span></span>

<span data-ttu-id="7f41a-146">หลังจากที่คุณมีโทเค็นการเข้าถึง คุณจะสามารถโทรหา Power BI REST API เพื่อฝังเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="7f41a-146">Now that you have the access token, you can call the Power BI REST API to embed content.</span></span>

<span data-ttu-id="7f41a-147">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7f41a-147">More questions?</span></span> [<span data-ttu-id="7f41a-148">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="7f41a-148">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)