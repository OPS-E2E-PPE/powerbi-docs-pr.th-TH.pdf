---
title: รับชุดข้อมูลเพื่อเพิ่มแถวในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: การฝึกปฏิบัติสำหรับการส่งข้อมูล - รับชุดข้อมูลเพื่อเพิ่มแถวลงในตาราง Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: madia
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: tutorial
ms.date: 02/05/2019
ms.openlocfilehash: e1be761f68dfcd58de8623618acd859694b95bde
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887465"
---
# <a name="step-4-get-a-dataset-to-add-rows-into-a-power-bi-table"></a><span data-ttu-id="1a6f7-104">ขั้นตอนที่ 4: รับชุดข้อมูลเพื่อเพิ่มแถวลงในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-104">Step 4: Get a dataset to add rows into a Power BI table</span></span>

<span data-ttu-id="1a6f7-105">บทความนี้เป็นส่วนหนึ่งของคำแนะนำทีละขั้นตอนเพื่อ[ส่งข้อมูลไปยังชุดข้อมูล](walkthrough-push-data.md)</span><span class="sxs-lookup"><span data-stu-id="1a6f7-105">This article is part of a step-by-step walkthrough to [push data into a dataset](walkthrough-push-data.md).</span></span>

<span data-ttu-id="1a6f7-106">ใน **ขั้นตอนที่ 3** เป็นขั้นตอนการส่งข้อมูลไปยังชุดข้อมูล [สร้างชุดข้อมูลใน Power BI](walkthrough-push-data-create-dataset.md)คุณเรียกใช้การดำเนินการ [สร้างชุดข้อมูล](/rest/api/power-bi/datasets)เพื่อสร้างชุดข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-106">In **step 3** of Push data into a dataset, [Create a dataset in Power BI](walkthrough-push-data-create-dataset.md), you called the [Create Dataset](/rest/api/power-bi/datasets) operation to create a dataset in Power BI.</span></span> <span data-ttu-id="1a6f7-107">ในขั้นตอนนี้ ให้คุณใช้การดำเนินการ[รับชุดข้อมูล](/rest/api/power-bi/datasets/getdatasets)และ Newtonsoft.Json เพื่อรับรหัสชุดข้อมูล คุณสามารถใช้รหัสชุดข้อมูลในขั้นตอนที่ 4 เพื่อเพิ่มแถวไปยังชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-107">In this step, you use the [Get Datasets](/rest/api/power-bi/datasets/getdatasets) operation and Newtonsoft.Json to get a dataset id. You use the dataset id in step 4 to add rows to a dataset.</span></span> 

<span data-ttu-id="1a6f7-108">เมื่อต้องส่งข้อมูลไปยังชุดข้อมูล Power BI คุณจำเป็นต้องอ้างอิงตารางในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-108">To push data into a Power BI dataset, you need to reference the table in the dataset.</span></span> <span data-ttu-id="1a6f7-109">เมื่อต้องการอ้างอิงตารางในชุดข้อมูล ก่อนอื่นคุณต้องได้รับ **รหัสชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1a6f7-109">To reference a table in a dataset, you first need to get a **Dataset ID**.</span></span> <span data-ttu-id="1a6f7-110">คุณได้รับ **รหัสชุดข้อมูล** โดยใช้การดำเนินการ [รับชุดข้อมูล](/rest/api/power-bi/datasets/getdatasets)</span><span class="sxs-lookup"><span data-stu-id="1a6f7-110">You get a **Dataset ID** using the [Get Datasets](/rest/api/power-bi/datasets/getdatasets) operation.</span></span> <span data-ttu-id="1a6f7-111">การดำเนินการ **รับชุดข้อมูล** จะส่งคืนสตริง JSON ที่ประกอบด้วยรายการของชุดข้อมูลทั้งหมดใน Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-111">The **Get Datasets** operation returns a JSON string containing a list of all datasets in Power BI.</span></span> <span data-ttu-id="1a6f7-112">วิธีแนะนำในการยกเลิกการจัดลำดับสตริง JSON อยู่ใน[Newtonsoft.Json](https://www.newtonsoft.com/json)</span><span class="sxs-lookup"><span data-stu-id="1a6f7-112">The recommended way to deserialize a JSON string is with [Newtonsoft.Json](https://www.newtonsoft.com/json).</span></span>

<span data-ttu-id="1a6f7-113">นี่คือวิธีที่คุณได้รับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-113">Here's how you get a dataset.</span></span>

## <a name="get-a-power-bi-dataset"></a><span data-ttu-id="1a6f7-114">รับชุดข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-114">Get a Power BI dataset</span></span>

> <span data-ttu-id="1a6f7-115">**หมายเหตุ**: ก่อนคุณเริ่มต้นใช้งาน ตรวจสอบให้แน่ใจว่า คุณดำเนินการตามขั้นตอนก่อนหน้านี้ในคำแนะนำการ [ส่งข้อมูล](walkthrough-push-data.md)ลงในชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-115">**NOTE**: Before you get started, make sure you have followed the previous steps in the [push data into a dataset](walkthrough-push-data.md) walkthrough.</span></span>

1. <span data-ttu-id="1a6f7-116">ในโครงการแอปพลิเคชันคอนโซลที่คุณสร้างในขั้นตอนที่ 2: คำแนะนำการส่งข้อมูล[รับโทเค็นการเข้าถึงการรับรองความถูกต้อง](walkthrough-push-data-get-token.md)ติดตั้งแพคเกจ Newtonsoft.Json NuGet</span><span class="sxs-lookup"><span data-stu-id="1a6f7-116">In the Console Application project you created in Step 2: Walkthrough to push data, [Get an authentication access token](walkthrough-push-data-get-token.md), install the Newtonsoft.Json NuGet package.</span></span> <span data-ttu-id="1a6f7-117">นี่คือวิธีการติดตั้งแพคเกจ:</span><span class="sxs-lookup"><span data-stu-id="1a6f7-117">Here's how to install the package:</span></span>

     <span data-ttu-id="1a6f7-118">a.</span><span class="sxs-lookup"><span data-stu-id="1a6f7-118">a.</span></span> <span data-ttu-id="1a6f7-119">ใน Studio Visual 2015 เลือก **เครื่องมือ** > **ตัวจัดการแพคเกจ NuGet** > **คอนโซลตัวจัดการแพคเกจ**</span><span class="sxs-lookup"><span data-stu-id="1a6f7-119">In Visual Studio 2015, choose **Tools** > **NuGet Package Manager** > **Package Manager Console**.</span></span>

     <span data-ttu-id="1a6f7-120">b.</span><span class="sxs-lookup"><span data-stu-id="1a6f7-120">b.</span></span> <span data-ttu-id="1a6f7-121">ใน **คอนโซล Manager แพคเกจ** ใส่ Newtonsoft.Json แพคเกจติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="1a6f7-121">In **Package Manager Console**, enter Install-Package Newtonsoft.Json.</span></span>
2. <span data-ttu-id="1a6f7-122">หลังจากติดตั้งแพคเกจแล้ว เพิ่ม **การใช้ Newtonsoft.Json;** ไปยัง Program.cs</span><span class="sxs-lookup"><span data-stu-id="1a6f7-122">After the package is installed, add **using Newtonsoft.Json;** to Program.cs.</span></span>
3. <span data-ttu-id="1a6f7-123">ใน Program.cs เพิ่มรหัสด้านล่างเพื่อรับ **รหัสชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1a6f7-123">In Program.cs, add the code below to get a **Dataset ID**.</span></span>
4. <span data-ttu-id="1a6f7-124">เรียกใช้แอปคอนโซลนี้ และเข้าสู่ระบบด้วยบัญชี Power BI ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1a6f7-124">Run the Console App, and login to your Power BI account.</span></span> <span data-ttu-id="1a6f7-125">คุณจะเห็น **รหัสชุดข้อมูล:** ตามด้วยรหัสในหน้าต่างคอนโซล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-125">You should see **Dataset ID:** followed by an id in the Console Window.</span></span>

<span data-ttu-id="1a6f7-126">**รับตัวอย่างเป็นชุดข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="1a6f7-126">**Sample get a dataset**</span></span>

<span data-ttu-id="1a6f7-127">เพิ่มรหัสนี้ลงใน Program.cs</span><span class="sxs-lookup"><span data-stu-id="1a6f7-127">Add this code into Program.cs.</span></span>

* <span data-ttu-id="1a6f7-128">ใน static void Main(string[] args):</span><span class="sxs-lookup"><span data-stu-id="1a6f7-128">In static void Main(string[] args):</span></span>
  
  ```csharp
  static void Main(string[] args)
  {
  
    //Get an authentication access token
    token = GetToken();
  
    //Create a dataset in Power BI
    CreateDataset();
  
    //Get a dataset to add rows into a Power BI table
    string datasetId = GetDataset();
  }
  ```
* <span data-ttu-id="1a6f7-129">เพิ่มวิธีการ GetDatset():</span><span class="sxs-lookup"><span data-stu-id="1a6f7-129">Add a GetDatset() method:</span></span>
  
  ```csharp
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
  ```

<span data-ttu-id="1a6f7-130">ขั้นตอนถัดไปจะแสดงวิธีการ[เพิ่มแถวลงในตาราง Power BI](walkthrough-push-data-add-rows.md)</span><span class="sxs-lookup"><span data-stu-id="1a6f7-130">The next step shows you how to [add rows to a Power BI table](walkthrough-push-data-add-rows.md).</span></span>

<span data-ttu-id="1a6f7-131">ด้านล่างนี้คือการ[รายการหัสที่สมบูรณ์](#code)</span><span class="sxs-lookup"><span data-stu-id="1a6f7-131">Below is the [complete code listing](#code).</span></span>

<a name="code"/>

## <a name="complete-code-listing"></a><span data-ttu-id="1a6f7-132">รายการรหัสเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="1a6f7-132">Complete code listing</span></span>

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
    }
}
```

## <a name="next-steps"></a><span data-ttu-id="1a6f7-133">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="1a6f7-133">Next steps</span></span>

* [<span data-ttu-id="1a6f7-134">เพิ่มแถวในตาราง Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-134">Add rows to a Power BI table</span></span>](walkthrough-push-data-add-rows.md)  
* [<span data-ttu-id="1a6f7-135">Newtonsoft.Json</span><span class="sxs-lookup"><span data-stu-id="1a6f7-135">Newtonsoft.Json</span></span>](https://www.newtonsoft.com/json)  
* [<span data-ttu-id="1a6f7-136">รับชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="1a6f7-136">Get Datasets</span></span>](/rest/api/power-bi/datasets/getdatasets)  
* [<span data-ttu-id="1a6f7-137">ส่งข้อมูลไปยัง Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-137">Push data into Power BI</span></span>](walkthrough-push-data.md)  
* [<span data-ttu-id="1a6f7-138">ภาพรวมของ Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="1a6f7-138">Overview of Power BI REST API</span></span>](overview-of-power-bi-rest-api.md)  
* [<span data-ttu-id="1a6f7-139">การอ้างอิง Power BI REST API</span><span class="sxs-lookup"><span data-stu-id="1a6f7-139">Power BI REST API reference</span></span>](/rest/api/power-bi/)  

<span data-ttu-id="1a6f7-140">คุณมีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1a6f7-140">More questions?</span></span> [<span data-ttu-id="1a6f7-141">ลองไปที่ชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="1a6f7-141">Try the Power BI Community</span></span>](https://community.powerbi.com/)