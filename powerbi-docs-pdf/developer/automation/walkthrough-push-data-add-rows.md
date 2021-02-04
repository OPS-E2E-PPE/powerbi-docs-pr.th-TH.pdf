---
title: เพิ่มแถวลงไปยังตารางในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: การฝึกปฏิบัติสำหรับการส่งข้อมูล - เพิ่มแถวลงในตาราง Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.date: 02/05/2019
ms.openlocfilehash: b34bc292d832938f34766ef94c5d9addd7b9e271
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887557"
---
# <a name="step-5-add-rows-to-a-power-bi-table"></a><span data-ttu-id="79d5c-104">ขั้นตอนที่ 5: เพิ่มแถวในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="79d5c-104">Step 5: Add rows to a Power BI table</span></span>

<span data-ttu-id="79d5c-105">บทความนี้เป็นส่วนหนึ่งของคำแนะนำทีละขั้นตอนเพื่อ[ส่งข้อมูลไปยังชุดข้อมูล](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="79d5c-105">This article is part of a step-by-step walkthrough to [push data into a dataset](walkthrough-push-data.md).</span></span>

<span data-ttu-id="79d5c-106">ใน **ขั้นตอนที่ 4** เป็นการส่งข้อมูลไปยังชุดข้อมูล [รับชุดข้อมูลเพื่อเพิ่มแถวลงในตาราง Power BI](walkthrough-push-data-get-datasets.md)คุณใช้การดำนเนินการ [รับชุดข้อมูล](/rest/api/power-bi/datasets/getdatasets)และ Newtonsoft.Json เพื่อรับรหัสชุดข้อมูล ในขั้นตอนนี้ คุณใช้รหัสชุดข้อมูลกับการดำเนินการ [โพสต์แถว](/rest/api/power-bi/pushdatasets/datasets_postrows) เพื่อเพิ่มแถวไปยัง **ชุดข้อมูล** Power BI</span><span class="sxs-lookup"><span data-stu-id="79d5c-106">In **step 4** of Push data into a dataset, [Get a dataset to add rows into a Power BI table](walkthrough-push-data-get-datasets.md), you used the [Get Datasets](/rest/api/power-bi/datasets/getdatasets) operation and Newtonsoft.Json to get a dataset id. In this step, you use the dataset id with the [PostRows](/rest/api/power-bi/pushdatasets/datasets_postrows) operation to add rows to a **Power BI** dataset.</span></span> 

<span data-ttu-id="79d5c-107">เมื่อคุณเรียกใช้การดำเนินการ[โพสต์แถว](/rest/api/power-bi/pushdatasets/datasets_postrows) คุณเพิ่มแถวไปยังชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="79d5c-107">When you call the [PostRows](/rest/api/power-bi/pushdatasets/datasets_postrows) operation, you add rows to a dataset.</span></span>

![เพิ่มแถว](media/walkthrough-push-data-add-rows/powerbi-developer-add-rows.png)

<span data-ttu-id="79d5c-109">นี่คือวิธีการเพิ่มแถวไปยังชุดข้อมูลโดยใช้ Power BI API</span><span class="sxs-lookup"><span data-stu-id="79d5c-109">Here's how to add rows to a dataset using the Power BI API.</span></span>

## <a name="add-rows-to-a-power-bi-table"></a><span data-ttu-id="79d5c-110">เพิ่มแถวในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="79d5c-110">Add rows to a Power BI table</span></span>

> [!NOTE]
> <span data-ttu-id="79d5c-111">ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่า คุณดำเนินตามขั้นตอนก่อนหน้านี้ในการฝึกปฏิบัติ[พุชข้อมูลลงในชุดข้อมูล](walkthrough-push-data.md)แล้ว</span><span class="sxs-lookup"><span data-stu-id="79d5c-111">Before you get started, make sure you have followed the previous steps in the [push data into a dataset](walkthrough-push-data.md) walkthrough.</span></span>

1. <span data-ttu-id="79d5c-112">ในแอปพลิเคชันคอนโซลคุณสร้างในขั้นตอนที่ 2: [รับโทเค็นการเข้าถึงการรับรองความถูกต้อง](walkthrough-push-data-get-token.md) เพิ่มโค้ดที่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="79d5c-112">In the Console Application project you created in Step 2: Walkthrough to push data, [Get an authentication access token](walkthrough-push-data-get-token.md), add the code below.</span></span>
2. <span data-ttu-id="79d5c-113">เรียกใช้แอปคอนโซล และเข้าสู่บัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="79d5c-113">Run the Console App, and login to your Power BI account.</span></span> <span data-ttu-id="79d5c-114">คุณจะเห็น **แถวที่เพิ่ม** ในหน้าต่างคอนโซล</span><span class="sxs-lookup"><span data-stu-id="79d5c-114">You should see **Rows Added** in the Console Window.</span></span> <span data-ttu-id="79d5c-115">คุณยังสามารถลงชื่อเข้าใช้ Power BI เพื่อดูแถวที่เพิ่มลงในชุดข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="79d5c-115">You can also login to Power BI to see the rows added to the dataset.</span></span>

<span data-ttu-id="79d5c-116">**ตัวอย่างการส่งข้อมูลไปยังชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="79d5c-116">**Sample push data into a dataset**</span></span>

<span data-ttu-id="79d5c-117">เพิ่มรหัสนี้ลงใน Program.cs</span><span class="sxs-lookup"><span data-stu-id="79d5c-117">Add this code into Program.cs.</span></span>

* <span data-ttu-id="79d5c-118">ค่าคงที่เพื่อยกเลิก Main(string[] args):</span><span class="sxs-lookup"><span data-stu-id="79d5c-118">In static void Main(string[] args):</span></span>
  
  ```csharp
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

  ```
* <span data-ttu-id="79d5c-119">เพิ่มวิธีการ AddRows():</span><span class="sxs-lookup"><span data-stu-id="79d5c-119">Add an AddRows() method:</span></span>

```csharp
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
```

<span data-ttu-id="79d5c-120">ด้านล่างนี้คือรายการรหัสที่เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="79d5c-120">Below is the complete code listing.</span></span>

## <a name="complete-code-listing"></a><span data-ttu-id="79d5c-121">รายการรหัสเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="79d5c-121">Complete code listing</span></span>

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

            #region Create a dataset in a Power BI
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

<span data-ttu-id="79d5c-122">แม้ว่า เราระบุว่าเรา **_//รับ id แรก_** ในรหัสข้างต้น สิ่งที่ต้องทำคือค้นหาชุดข้อมูลตามชื่อ</span><span class="sxs-lookup"><span data-stu-id="79d5c-122">Although, we specify that we **_//Get the first id_** in the code above, the correct thing to do is search the dataset by name.</span></span>

## <a name="next-steps"></a><span data-ttu-id="79d5c-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="79d5c-123">Next steps</span></span>
[<span data-ttu-id="79d5c-124">พุชข้อมูลลงในแดชบอร์ด Power BI</span><span class="sxs-lookup"><span data-stu-id="79d5c-124">Push data into a Power BI Dashboard</span></span>](walkthrough-push-data.md)  
[<span data-ttu-id="79d5c-125">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="79d5c-125">Overview of Power BI REST API</span></span>](overview-of-power-bi-rest-api.md)  
[<span data-ttu-id="79d5c-126">การอ้างอิง Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="79d5c-126">Power BI REST API reference</span></span>](/rest/api/power-bi/)  
<span data-ttu-id="79d5c-127">คุณมีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="79d5c-127">More questions?</span></span> [<span data-ttu-id="79d5c-128">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="79d5c-128">Try the Power BI Community</span></span>](https://community.powerbi.com/)
