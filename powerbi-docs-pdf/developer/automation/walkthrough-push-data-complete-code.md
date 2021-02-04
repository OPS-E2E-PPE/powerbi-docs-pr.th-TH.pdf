---
title: ทำรายการโค้ดให้เสร็จสมบูรณ์ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: การฝึกปฏิบัติสำหรับการส่งข้อมูล - ทำรายการโค้ดให้เสร็จสมบูรณ์ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: conceptual
ms.date: 02/05/2019
ms.openlocfilehash: d478c742112c15c80657ec424f5a4d6739a3c6d7
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887488"
---
# <a name="push-data-to-a-dataset-complete-code-listing"></a><span data-ttu-id="342df-104">ส่งข้อมูลไปยังชุดข้อมูลรายการรหัสที่สร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="342df-104">Push data to a dataset complete code listing</span></span>

<span data-ttu-id="342df-105">บทความนี้เป็นส่วนหนึ่งของคำแนะนำทีละขั้นตอนเพื่อ[ส่งข้อมูลไปยังชุดข้อมูล](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="342df-105">This article is part of a step-by-step walkthrough to [push data into a dataset](walkthrough-push-data.md).</span></span>

<span data-ttu-id="342df-106">หลังจากที่คุณทำตามขั้นตอนที่ 2 ถึง 5 ในการ **ส่งข้อมูลไปยังชุดข้อมูล** รหัสแหล่งที่มาที่สมบูรณ์ของคุณควรมีลักษณะดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="342df-106">After you follow Steps 2 to 5 in **Push data into a dataset**, your complete source code should look like the following.</span></span>

## <a name="push-data-to-dataset-code"></a><span data-ttu-id="342df-107">ส่งข้อมูลไปยังรหัสชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="342df-107">Push data to dataset code</span></span>

```csharp
      using System;
      using Microsoft.IdentityModel.Clients.ActiveDirectory;
      using System.Net;
      using System.IO;
      using Newtonsoft.Json;

      namespace walkthrough_push_data
      {
          class Program
          {
              private static string token = string.Empty;

              static void Main(string[] args)
              {

                  //Get an authentication access token
                  token = GetToken();

                  //Create a dataset in Power BI
                  CreateDataset();

                  //Get a dataset to add rows into a Power BI table
                  string datasetId = GetDataset();

                  //Add rows to a Power BI table
                  AddRows(datasetId, "Product");

              }

              #region Get an authentication access token
              private static string GetToken()
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
                  string token = authContext.AcquireToken(resourceUri, clientID, new Uri(redirectUri)).AccessToken;

                  Console.WriteLine(token);
                  Console.ReadLine();

                  return token;
              }

              #endregion

              #region Create a dataset in Power BI
              private static void CreateDataset()
              {
                  //TODO: Add using System.Net and using System.IO

                  string powerBIDatasetsApiUrl = "https://api.powerbi.com/v1.0/myorg/datasets";
                  //POST web request to create a dataset.
                  //To create a Dataset in a group, use the Groups uri: https://api.PowerBI.com/v1.0/myorg/groups/{group_id}/datasets
                  HttpWebRequest request = System.Net.WebRequest.Create(powerBIDatasetsApiUrl) as System.Net.HttpWebRequest;
                  request.KeepAlive = true;
                  request.Method = "POST";
                  request.ContentLength = 0;
                  request.ContentType = "application/json";

                  //Add token to the request header
                  request.Headers.Add("Authorization", String.Format("Bearer {0}", token));

                  //Create dataset JSON for POST request
                  string datasetJson = "{\"name\": \"SalesMarketing\", \"tables\": " +
                      "[{\"name\": \"Product\", \"columns\": " +
                      "[{ \"name\": \"ProductID\", \"dataType\": \"Int64\"}, " +
                      "{ \"name\": \"Name\", \"dataType\": \"string\"}, " +
                      "{ \"name\": \"Category\", \"dataType\": \"string\"}," +
                      "{ \"name\": \"IsCompete\", \"dataType\": \"bool\"}," +
                      "{ \"name\": \"ManufacturedOn\", \"dataType\": \"DateTime\"}" +
                      "]}]}";

                  //POST web request
                  byte[] byteArray = System.Text.Encoding.UTF8.GetBytes(datasetJson);
                  request.ContentLength = byteArray.Length;

                  //Write JSON byte[] into a Stream
                  using (Stream writer = request.GetRequestStream())
                  {
                      writer.Write(byteArray, 0, byteArray.Length);

                      var response = (HttpWebResponse)request.GetResponse();

                      Console.WriteLine(string.Format("Dataset {0}", response.StatusCode.ToString()));

                      Console.ReadLine();
                  }
              }
              #endregion

              #region Get a dataset to add rows into a Power BI table
              private static string GetDataset()
              {
                  string powerBIDatasetsApiUrl = "https://api.powerbi.com/v1.0/myorg/datasets";
                  //POST web request to create a dataset.
                  //To create a Dataset in a group, use the Groups uri: https://api.PowerBI.com/v1.0/myorg/groups/{group_id}/datasets
                  HttpWebRequest request = System.Net.WebRequest.Create(powerBIDatasetsApiUrl) as System.Net.HttpWebRequest;
                  request.KeepAlive = true;
                  request.Method = "GET";
                  request.ContentLength = 0;
                  request.ContentType = "application/json";

                  //Add token to the request header
                  request.Headers.Add("Authorization", String.Format("Bearer {0}", token));

                  string datasetId = string.Empty;
                  //Get HttpWebResponse from GET request
                  using (HttpWebResponse httpResponse = request.GetResponse() as System.Net.HttpWebResponse)
                  {
                      //Get StreamReader that holds the response stream
                      using (StreamReader reader = new System.IO.StreamReader(httpResponse.GetResponseStream()))
                      {
                          string responseContent = reader.ReadToEnd();

                          //TODO: Install NuGet Newtonsoft.Json package: Install-Package Newtonsoft.Json
                          //and add using Newtonsoft.Json
                          var results = JsonConvert.DeserializeObject<dynamic>(responseContent);

                          //Get the first id
                          datasetId = results["value"][0]["id"];

                          Console.WriteLine(String.Format("Dataset ID: {0}", datasetId));
                          Console.ReadLine();

                          return datasetId;
                      }
                  }
              }
              #endregion

              #region Add rows to a Power BI table
              private static void AddRows(string datasetId, string tableName)
              {
                  string powerBIApiAddRowsUrl = String.Format("https://api.powerbi.com/v1.0/myorg/datasets/{0}/tables/{1}/rows", datasetId, tableName);

                  //POST web request to add rows.
                  //To add rows to a dataset in a group, use the Groups uri: https://api.powerbi.com/v1.0/myorg/groups/{group_id}/datasets/{dataset_id}/tables/{table_name}/rows
                  //Change request method to "POST"
                  HttpWebRequest request = System.Net.WebRequest.Create(powerBIApiAddRowsUrl) as System.Net.HttpWebRequest;
                  request.KeepAlive = true;
                  request.Method = "POST";
                  request.ContentLength = 0;
                  request.ContentType = "application/json";

                  //Add token to the request header
                  request.Headers.Add("Authorization", String.Format("Bearer {0}", token));

                  //JSON content for product row
                  string rowsJson = "{\"rows\":" +
                      "[{\"ProductID\":1,\"Name\":\"Adjustable Race\",\"Category\":\"Components\",\"IsCompete\":true,\"ManufacturedOn\":\"07/30/2014\"}," +
                      "{\"ProductID\":2,\"Name\":\"LL Crankarm\",\"Category\":\"Components\",\"IsCompete\":true,\"ManufacturedOn\":\"07/30/2014\"}," +
                      "{\"ProductID\":3,\"Name\":\"HL Mountain Frame - Silver\",\"Category\":\"Bikes\",\"IsCompete\":true,\"ManufacturedOn\":\"07/30/2014\"}]}";

                  //POST web request
                  byte[] byteArray = System.Text.Encoding.UTF8.GetBytes(rowsJson);
                  request.ContentLength = byteArray.Length;

                  //Write JSON byte[] into a Stream
                  using (Stream writer = request.GetRequestStream())
                  {
                      writer.Write(byteArray, 0, byteArray.Length);

                      var response = (HttpWebResponse)request.GetResponse();

                      Console.WriteLine("Rows Added");

                      Console.ReadLine();
                  }
              }

              #endregion
          }
      }
```

## <a name="next-steps"></a><span data-ttu-id="342df-108">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="342df-108">Next steps</span></span>

* [<span data-ttu-id="342df-109">ส่งข้อมูลลงในชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="342df-109">Push data into a Power BI dataset</span></span>](walkthrough-push-data.md)
* [<span data-ttu-id="342df-110">ลงทะเบียนแอปกับ Azure AD</span><span class="sxs-lookup"><span data-stu-id="342df-110">Register an app with Azure AD</span></span>](../embedded/register-app.md)  
* [<span data-ttu-id="342df-111">รับโทเค็นการเข้าถึงการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="342df-111">Get an authentication access token</span></span>](walkthrough-push-data-get-token.md)  
* [<span data-ttu-id="342df-112">สร้างชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="342df-112">Create a dataset in Power BI</span></span>](walkthrough-push-data-create-dataset.md)  
* [<span data-ttu-id="342df-113">รับชุดข้อมูลเพื่อเพิ่มแถวลงในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="342df-113">Get a dataset to add rows into a Power BI table</span></span>](walkthrough-push-data-get-datasets.md)  
* [<span data-ttu-id="342df-114">เพิ่มแถวในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="342df-114">Add rows to a Power BI table</span></span>](walkthrough-push-data-add-rows.md)  
* [<span data-ttu-id="342df-115">การอ้างอิง Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="342df-115">Power BI REST API reference</span></span>](/rest/api/power-bi/)  
* [<span data-ttu-id="342df-116">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="342df-116">Overview of Power BI REST API</span></span>](overview-of-power-bi-rest-api.md)  

<span data-ttu-id="342df-117">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="342df-117">More questions?</span></span> [<span data-ttu-id="342df-118">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="342df-118">Try the Power BI Community</span></span>](https://community.powerbi.com/)