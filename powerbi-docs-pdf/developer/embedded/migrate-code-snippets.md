---
title: ส่วนย่อยของโค้ดสำหรับการโยกย้ายเนื้อหาจากคอลเลกชันพื้นที่ทำงานไปยังโซลูชันการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: ต่อไปนี้คือโค้ดบางอย่างของการดำเนินงานพื้นฐานที่จำเป็นสำหรับการโยกย้ายเนื้อหา เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 02/05/2019
ms.openlocfilehash: f6b6023ac77d007b07662e200d6f165d56d67628
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888730"
---
# <a name="code-snippets-for-migrating-content-from-power-bi-workspace-collection"></a><span data-ttu-id="8e018-104">โค้ดสำหรับการโยกย้ายเนื้อหาจากคอลเลกชันพื้นที่ทำงานของ Power BI</span><span class="sxs-lookup"><span data-stu-id="8e018-104">Code snippets for migrating content from Power BI Workspace Collection</span></span>

<span data-ttu-id="8e018-105">ต่อไปนี้คือโค้ดบางอย่างของการดำเนินงานพื้นฐานที่จำเป็นสำหรับการโยกย้ายเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="8e018-105">Here are some code snippets of basic operations needed for content migration.</span></span> <span data-ttu-id="8e018-106">สำหรับขั้นตอนที่เกี่ยวข้องกับรายงานบางชนิด ดู[วิธีการโยกย้ายเนื้อหาคอลเลกชันของพื้นที่ทำงาน Power BI ไปยัง Power BI Embedded](migrate-from-powerbi-embedded.md#content-migration)</span><span class="sxs-lookup"><span data-stu-id="8e018-106">For related flows for certain report types, see [How to migrate Power BI workspace collection content to Power BI Embedded](migrate-from-powerbi-embedded.md#content-migration).</span></span>

<span data-ttu-id="8e018-107">A **เครื่องมือการโยกย้าย** จะพร้อมใช้งานเพื่อให้คุณใช้เพื่อช่วยเหลือเกี่ยวกับการคัดลอกเนื้อหาจาก Power BI Embedded (PaaS) ไปยังบริการ Power BI (SaaS)</span><span class="sxs-lookup"><span data-stu-id="8e018-107">A **migration tool** is available for you to use in order to assist with copying content from Power BI Embedded (PaaS) to the Power BI service (SaaS).</span></span> <span data-ttu-id="8e018-108">โดยเฉพาะอย่างยิ่ง ถ้าคุณมีเนื้อหาจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="8e018-108">Especially if you have a lot of content.</span></span> <span data-ttu-id="8e018-109">สำหรับข้อมูลเพิ่มเติม ดู[เครื่องมือการโยกย้ายของ Power BI Embedded](migrate-tool.md)</span><span class="sxs-lookup"><span data-stu-id="8e018-109">For more information, see [Power BI Embedded migration tool](migrate-tool.md).</span></span>

<span data-ttu-id="8e018-110">รหัสด้านล่างนี้คือ ตัวอย่างที่ใช้ C# และ[Power BI .NET SDK](https://www.nuget.org/profiles/powerbi)</span><span class="sxs-lookup"><span data-stu-id="8e018-110">The code below are examples using C# and the [Power BI .NET SDK](https://www.nuget.org/profiles/powerbi).</span></span>

<span data-ttu-id="8e018-111">ตรวจสอบให้แน่ใจว่า คุณกำลังใช้ใน namespace ต่อไปนี้เพื่อดำเนินการโค้ดด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="8e018-111">Make sure you are using the following namespaces to execute the code snippets below.</span></span>

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V1;
using Microsoft.PowerBI.Api.V1.Models;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;
using Microsoft.Rest;
using Microsoft.Rest.Serialization;
using Newtonsoft.Json;
using Newtonsoft.Json.Linq;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Net;
using System.Net.Http;
using System.Net.Http.Headers;
using System.Text;
using System.Threading.Tasks;
```

## <a name="export-report-from-paas-workspace"></a><span data-ttu-id="8e018-112">ส่งออกรายงานจากพื้นที่ทำงาน PaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-112">Export report from PaaS workspace</span></span>

```csharp
    // Create a token credentials with "AppKey" type
    var credentials = new TokenCredentials(<myAppKey==>, "AppKey");

    // Instantiate your Power BI client passing in the required credentials
    var client = new PowerBIClient(credentials);

    client.BaseUri = new Uri("https://api.powerbi.com");

    var response = client.Reports.ExportReportWithHttpMessagesAsync(<myWorkspaceCollectionName>, <myWorkspaceId>, <myReportId>);

    if (response.Result.Response.StatusCode == HttpStatusCode.OK)
    {
        var stream = response.Result.Response.Content.ReadAsStreamAsync();

        using (FileStream fileStream = File.Create(@"C:\Migration\myfile.pbix"))
        {
            stream.Result.CopyTo(fileStream);
            fileStream.Close();
        }
    }
```

## <a name="import-report-to-saas-workspace"></a><span data-ttu-id="8e018-113">นำเข้ารายงานไปยังพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-113">Import report to SaaS workspace</span></span>

```csharp
    AuthenticationContext authContext = new AuthenticationContext("https://login.microsoftonline.net/common/");
    var PBISaaSAuthResult = authContext.AcquireToken("https://analysis.windows.net/powerbi/api", <myClientId>, new Uri("urn:ietf:wg:oauth:2.0:oob"), PromptBehavior.Always);
    var credentials = new TokenCredentials(PBISaaSAuthResult.AccessToken);
    var client = new PowerBIClient(new Uri($"{"https://api.powerbi.com"}"), credentials);
    using (var file = File.Open(@"C:\Migration\myfile.pbix", FileMode.Open))
    {
        client.Imports.PostImportWithFileInGroup(<mySaaSWorkspaceId>, file, "importedreport", "Abort");
        while (true) ;
    }
```

## <a name="extract-directquery-connection-string-from-paas-report"></a><span data-ttu-id="8e018-114">สำหรับตัวอย่าง ดูที่สตริงการเชื่อมต่อ “DirectQuery ที่แยกออก” จากรายงาน PaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-114">Extract DirectQuery connection string from PaaS report</span></span>

<span data-ttu-id="8e018-115">นี่คือการปรับปรุง PBIX หลังจากการโยกย้ายไปยัง SaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-115">This is for updating the PBIX after migrating to SaaS.</span></span>

```csharp
    // Extract connection string from PaaS - DirectQuery report
    // Create a token credentials with "AppKey" type
    var credentials = new TokenCredentials(<myAppKey==>, "AppKey");

    // Instantiate your Power BI client passing in the required credentials
    var client = new PowerBIClient(credentials);

    client.BaseUri = new Uri("https://api.powerbi.com");

    var reports = client.Reports.GetReports(<myWorkspaceCollectionName>, <myWorkspaceId>);

    Report report = reports.Value.FirstOrDefault(r => string.Equals(r.Id, <myReportId, StringComparison.OrdinalIgnoreCase));

    var datasource = client.Datasets.GetDatasources(<myWorkspaceCollectionName>, <myWorkspaceId>, report.DatasetId);
```

## <a name="update-directquery-connection-string-is-saas-workspace"></a><span data-ttu-id="8e018-116">การอัปเดตสตริงเชื่อมต่อ DirectQuery คือ พื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-116">Update DirectQuery connection string is SaaS workspace</span></span>

```csharp
    public class ConnectionString
    {
        [JsonProperty(PropertyName = "connectionString")]
        public string connection { get; set; }
    }

    AuthenticationContext authContext = new AuthenticationContext("https://login.microsoftonline.net/common/");
    var PBISaaSAuthResult = authContext.AcquireToken("https://analysis.windows.net/powerbi/api",<myclient_id>, new Uri("urn:ietf:wg:oauth:2.0:oob"), PromptBehavior.Always);
    var credentials = new TokenCredentials(PBISaaSAuthResult.AccessToken);
    var client = new PowerBIClient(new Uri($"{"https://api.powerbi.com"}"), credentials);

    ConnectionString connection = new ConnectionString() { connection = "data source = <server_name>; initial catalog = <db_name>; persist security info = True; encrypt = True; trustservercertificate = False" };

    client.Datasets.SetAllConnectionsInGroup(<myWorkspaceId>, <dataset_id>, connection);
```

## <a name="set-directquery-credentials-in-saas-workspace"></a><span data-ttu-id="8e018-117">ตั้งค่าข้อมูลประจำตัวของ DirectQuery ในพื้นที่ทำงาน SaaS</span><span class="sxs-lookup"><span data-stu-id="8e018-117">Set DirectQuery credentials in SaaS workspace</span></span>

<span data-ttu-id="8e018-118">ในส่วนย่อยนี้ เราจะใช้ข้อมูลประจำตัวการเข้ารหัสลับสำหรับความสะดวกสบาย ส่งข้อมูลประจำตัวเข้ารหัสลับได้รับการสนับสนุนเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8e018-118">In this snippet, we are using unencrypted credentials for simplicity, sending encrypted credentials is supported as well.</span></span>

```csharp
    public class ConnectionString
    {
        [JsonProperty(PropertyName = "connectionString")]
        public string connection { get; set; }
    }

    public class BasicCreds
    {
        [JsonProperty(PropertyName = "username")]
        public string user { get; set; }

        [JsonProperty(PropertyName = "password")]
        public string pwd { get; set; }
    }

    var basicCreds = new BasicCreds() { user = <sqldb_username>, pwd = <sqldb_password> };
    var body = new SetCredsRequestBody() { credentialType = "Basic", basicCredentials = basicCreds };

    var url = string.Format("https://api.powerbi.com/v1.0/myorg/gateways/{0}/datasources/{1}", <gateway_id>, <datasource_id>);
    var request = new HttpRequestMessage(new HttpMethod("PATCH"), url);
    // Set authorization header from you acquired Azure AD token
    AuthenticationContext authContext = new AuthenticationContext("https://login.microsoftonline.net/common/");
    var PBISaaSAuthResult = authContext.AcquireToken("https://analysis.windows.net/powerbi/api", <myclient_id>, new Uri("urn:ietf:wg:oauth:2.0:oob"), PromptBehavior.Always);

    request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", PBISaaSAuthResult.AccessToken);

    request.Content = new StringContent(JsonConvert.SerializeObject(body), Encoding.UTF8, "application/json");

    HttpClient simpleClient = new HttpClient();
    var response = await simpleClient.SendAsync(request);
```

## <a name="push-dataset-and-report"></a><span data-ttu-id="8e018-119">เผยแพร่ชุดข้อมูลและรายงาน</span><span class="sxs-lookup"><span data-stu-id="8e018-119">Push dataset and report</span></span>

<span data-ttu-id="8e018-120">คุณจะต้องสร้างรายงานสำหรับชุดข้อมูลสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8e018-120">You will need to rebuild the report for the created dataset.</span></span>

<span data-ttu-id="8e018-121">ในส่วนย่อยนี้ เราคาดว่าชุดข้อมูลที่สามารถผลักได้นั้นอยู่ในพื้นที่ทำงานภายในสภาพแวดล้อม SaaS อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="8e018-121">In this snippet, we assume that the pushable dataset is already in a workspace within the SaaS environment.</span></span> <span data-ttu-id="8e018-122">สำหรับข้อมูลเกี่ยวกับ push API ดูที่[ผลักข้อมูลลงในชุดข้อมูล Power BI](../automation/walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="8e018-122">For information about the push API, see [Push data into a Power BI dataset](../automation/walkthrough-push-data.md).</span></span>

```csharp
    var credentials = new TokenCredentials(<Your WSC access key>, "AppKey");

    // Instantiate your Power BI client passing in the required credentials
    var client = new Microsoft.PowerBI.Api.V1.PowerBIClient(credentials);
    client.BaseUri = new Uri("https://api.powerbi.com");

    // step 1 -> create dummy dataset at PaaS workspace
    var fileStream = File.OpenRead(<Path to your dummy dataset>);
    var import = client.Imports.PostImportWithFileAsync(<Your WSC NAME>, <Your workspace ID>, fileStream, "dummyDataset");
    while (import.Result.ImportState != "Succeeded" && import.Result.ImportState != "Failed")
    {
        import = client.Imports.GetImportByIdAsync(<Your WSC NAME>, <Your workspace ID>, import.Result.Id);
        Thread.Sleep(1000);
    }
    var dummyDatasetID = import.Result.Datasets[0].Id;

    // step 2 -> clone the pushable dataset and rebind to dummy dataset
    var cloneInfo = new Microsoft.PowerBI.Api.V1.Models.CloneReportRequest("pushableReportClone",null, dummyDatasetID);
    var clone = client.Reports.CloneReportAsync(<Your WSC NAME>, <Your workspace ID>, <Your pushable report ID>, cloneInfo);
    var pushableReportCloneID = clone.Result.Id;


    // step 3 -> Download the push API clone report with the dummy dataset
    var response = client.Reports.ExportReportWithHttpMessagesAsync(<Your WSC NAME>, <Your workspace ID>, pushableReportCloneID);
    if (response.Result.Response.StatusCode == HttpStatusCode.OK)
    {
        var stream = response.Result.Response.Content.ReadAsStreamAsync();
        using (fileStream = File.Create(@"C:\Migration\PushAPIReport.pbix"))
        {
            stream.Result.CopyTo(fileStream);
            fileStream.Close();
        }
    }

    // step 4 -> Upload dummy PBIX to SaaS workspace
    AuthenticationContext authContext = new AuthenticationContext("https://login.microsoftonline.net/common/");
    var PBISaaSAuthResult = authContext.AcquireToken("https://analysis.windows.net/powerbi/api", <Your client ID>, new Uri("urn:ietf:wg:oauth:2.0:oob"), PromptBehavior.Always);
    var credentialsSaaS = new TokenCredentials(PBISaaSAuthResult.AccessToken);
    var clientSaaS = new Microsoft.PowerBI.Api.V2.PowerBIClient(new Uri($"{"https://api.powerbi.com"}"), credentialsSaaS);
    using (var file = File.Open(@"C:\Migration\PushAPIReport.pbix", FileMode.Open))
    {

        var importSaaS = clientSaaS.Imports.PostImportWithFileAsyncInGroup(<Your GroupID>, file, "importedreport1", "Abort");
        while (importSaaS.Result.ImportState != "Succeeded" && importSaaS.Result.ImportState != "Failed")
        {
            importSaaS = clientSaaS.Imports.GetImportByIdAsync(importSaaS.Result.Id);
            Thread.Sleep(1000);
        }
        var importedreport1ID = importSaaS.Result.Reports[0].Id;


        // step 5 -> Rebind report to "real" push api dataset
        var rebindInfoSaaS = new Microsoft.PowerBI.Api.V2.Models.RebindReportRequest(<Your pushable dataset  ID at power bi>);
        var rebindSaaS = clientSaaS.Reports.RebindReportInGroupWithHttpMessagesAsync(<Your GroupID>, importedreport1ID, rebindInfoSaaS);

    }
```

## <a name="next-steps"></a><span data-ttu-id="8e018-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="8e018-123">Next steps</span></span>

[<span data-ttu-id="8e018-124">เครื่องมือการย้าย Power BI แบบฝัง</span><span class="sxs-lookup"><span data-stu-id="8e018-124">Power BI Embedded migration tool</span></span>](migrate-tool.md)  
[<span data-ttu-id="8e018-125">การฝังด้วย Power BI</span><span class="sxs-lookup"><span data-stu-id="8e018-125">Embedding with Power BI</span></span>](embedding.md)  
[<span data-ttu-id="8e018-126">วิธีการย้ายเนื้อหาคอลเลกชันพื้นที่ทำงานแบบฝัง Power BI ไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="8e018-126">How to migrate Power BI Embedded workspace collection content to Power BI</span></span>](migrate-from-powerbi-embedded.md)  
[<span data-ttu-id="8e018-127">วิธีฝัง แดชบอร์ด รายงาน และไทล์ Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e018-127">How to embed your Power BI dashboards, reports and tiles</span></span>](embed-sample-for-your-organization.md)  
[<span data-ttu-id="8e018-128">Power BI Premium คืออะไร</span><span class="sxs-lookup"><span data-stu-id="8e018-128">Power BI Premium - what is it?</span></span>](../../admin/service-premium-what-is.md)  
[<span data-ttu-id="8e018-129">JavaScript API Git repo</span><span class="sxs-lookup"><span data-stu-id="8e018-129">JavaScript API Git repo</span></span>](https://github.com/Microsoft/PowerBI-JavaScript)  
[<span data-ttu-id="8e018-130">Power BI C# Git repo</span><span class="sxs-lookup"><span data-stu-id="8e018-130">Power BI C# Git repo</span></span>](https://github.com/Microsoft/PowerBI-CSharp)  
[<span data-ttu-id="8e018-131">ตัวอย่างการฝัง JavaScript</span><span class="sxs-lookup"><span data-stu-id="8e018-131">JavaScript embed sample</span></span>](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[<span data-ttu-id="8e018-132">เอกสารบรรยายแนวความคิดของ Power BI Premium</span><span class="sxs-lookup"><span data-stu-id="8e018-132">Power BI Premium whitepaper</span></span>](https://aka.ms/pbipremiumwhitepaper)  

<span data-ttu-id="8e018-133">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8e018-133">More questions?</span></span> [<span data-ttu-id="8e018-134">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="8e018-134">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
