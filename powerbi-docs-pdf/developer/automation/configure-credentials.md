---
title: กำหนดค่าข้อมูลประจำตัวทางโปรแกรมสำหรับการวิเคราะห์แบบฝังตัวของ Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: วิธีการกำหนดค่าข้อมูลประจำตัวทางโปรแกรมเมื่อทำ Power BI ให้เป็นอัตโนมัติ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 06/23/2020
ms.openlocfilehash: c87ca689d804c909ca3a6ca9544ac1a4568c8b86
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97887649"
---
# <a name="configure-credentials-programmatically-for-power-bi"></a><span data-ttu-id="b3e9a-104">กำหนดค่าข้อมูลประจำตัวทางโปรแกรมสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="b3e9a-104">Configure credentials programmatically for Power BI</span></span>

<span data-ttu-id="b3e9a-105">ทำตามขั้นตอนในบทความนี้เพื่อกำหนดค่าข้อมูลประจำตัวทางโปรแกรมสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="b3e9a-105">Follow the steps in this article, to configure credentials programmatically for Power BI.</span></span>

>[!NOTE]
>* <span data-ttu-id="b3e9a-106">ผู้ใช้ที่เรียกต้องเป็นเจ้าของชุดข้อมูลหรือผู้ดูแลเกตเวย์ คุณยังสามารถใช้ [บริการหลัก](../embedded/embed-service-principal.md) ได้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-106">The calling user must be a dataset owner, or a gateway admin. You can also use a [service principal](../embedded/embed-service-principal.md).</span></span> <span data-ttu-id="b3e9a-107">ตัวอย่างเช่น บริการหลักสามารถเป็นเจ้าของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-107">For example, the service principal can be the dataset owner.</span></span>
>* <span data-ttu-id="b3e9a-108">แหล่งข้อมูลระบบคลาวด์ และข้อมูลประจำตัวที่สอดคล้องกันจะถูกจัดการในระดับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-108">Cloud data sources and their corresponding credentials are managed at the user level.</span></span>

## <a name="update-credentials-flow-for-data-sources"></a><span data-ttu-id="b3e9a-109">อัปเดตโฟลว์ข้อมูลประจำตัวสำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-109">Update credentials flow for data sources</span></span>

1. <span data-ttu-id="b3e9a-110">เรียกใช้ฟังก์ชัน[รับแหล่งข้อมูล](/rest/api/power-bi/datasets/getdatasourcesingroup)เพื่อค้นหาแหล่งข้อมูลของชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-110">Call [Get Datasources](/rest/api/power-bi/datasets/getdatasourcesingroup) to discover the data sources of the dataset.</span></span> <span data-ttu-id="b3e9a-111">ในเนื้อหาคำตอบสำหรับแต่ละแหล่งข้อมูล มีชนิด รายละเอียดการเชื่อมต่อ เกตเวย์ และรหัสแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-111">In the response body for each data source, are the type, connection details, gateway, and data source ID.</span></span>

    ```csharp
    // Select a datasource
    var datasources = pbiClient.Datasets.GetDatasources(datasetId).Value;
    var datasource = datasources.First();
    ```

2. <span data-ttu-id="b3e9a-112">สร้างข้อมูลประจำตัวของสตริงตาม[ตัวอย่างของแหล่งข้อมูลอัปเด](/rest/api/power-bi/gateways/updatedatasource)ทั้งนี้ขึ้นอยู่กับชนิดข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="b3e9a-112">Build credentials string according to [Update Datasource Examples](/rest/api/power-bi/gateways/updatedatasource) depending on the credentials type.</span></span>

    # <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-113">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-113">.NET SDK v3</span></span>](#tab/sdk3)

    ```csharp
    var credentials =  new BasicCredentials(username: "username", password :"*****");
    ```

    # <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-114">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-114">.NET SDK v2</span></span>](#tab/sdk2)

     ```csharp
    var credentials = "{\"credentialData\":[{\"name\":\"username\", \"value\":\"john\"},{\"name\":\"password\", \"value\":\"*****\"}]}";
    ```

    ---

    >[!NOTE]
    ><span data-ttu-id="b3e9a-115">หากคุณกำลังใช้แหล่งข้อมูลคลาวด์ อย่าทำตามขั้นตอนถัดไปในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-115">If you're using cloud data sources don't follow the next steps in this section.</span></span> <span data-ttu-id="b3e9a-116">ตั้งค่าข้อมูลประจำตัวโดยใช้ ID เกตเวย์และ ID แหล่งข้อมูลที่ได้รับในขั้นตอนที่ 1 โดยการเรียก [อัปเดตแหล่งข้อมูล](/rest/api/power-bi/gateways/updatedatasource)</span><span class="sxs-lookup"><span data-stu-id="b3e9a-116">Set the credentials using the gateway ID and data source ID obtained in step 1, by calling [Update Datasource](/rest/api/power-bi/gateways/updatedatasource).</span></span> 

3. <span data-ttu-id="b3e9a-117">เรียกใช้ฟังก์ชัน [รับเกตเวย์](/rest/api/power-bi/gateways/getgateways)เพื่อเรียกใช้คีย์สาธารณะของเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="b3e9a-117">Call [Get Gateway](/rest/api/power-bi/gateways/getgateways) to retrieve the gateway public key.</span></span>

    ```csharp
    var gateway = pbiClient.Gateways.GetGatewayById(datasource.GatewayId);
    ```

4. <span data-ttu-id="b3e9a-118">เข้ารหัสข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="b3e9a-118">Encrypt the credentials.</span></span>

    # <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-119">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-119">.NET SDK v3</span></span>](#tab/sdk3)

    ```csharp
    var credentialsEncryptor = new AsymmetricKeyEncryptor(gateway.publicKey);
    ```

    # <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-120">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-120">.NET SDK v2</span></span>](#tab/sdk2)

    <span data-ttu-id="b3e9a-121">เข้ารหัสสตริงข้อมูลประจำตัวกับคีย์สาธารณะของเกตเวย์จากขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-121">Encrypt the credentials string with the Gateway public key from step 2.</span></span> <span data-ttu-id="b3e9a-122">เกตเวย์เวอร์ชันที่แตกต่างกันอาจมีขนาดคีย์สาธารณะที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b3e9a-122">Different gateway versions may have different public key sizes.</span></span> <span data-ttu-id="b3e9a-123">อ้างอิงตัวอย่างต่อไปนี้ในรหัส SDK พร้อมใช้งานจาก[ที่เก็บ PowerBI-CSharp GitHub](https://github.com/microsoft/PowerBI-CSharp/tree/master/sdk/PowerBI.Api/Extensions):</span><span class="sxs-lookup"><span data-stu-id="b3e9a-123">Refer to the following examples in the SDK code, available from the [PowerBI-CSharp GitHub repository](https://github.com/microsoft/PowerBI-CSharp/tree/master/sdk/PowerBI.Api/Extensions):</span></span>
    * [<span data-ttu-id="b3e9a-124">AsymmetricKeyEncryptor.cs</span><span class="sxs-lookup"><span data-stu-id="b3e9a-124">AsymmetricKeyEncryptor.cs</span></span>](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AsymmetricKeyEncryptor.cs)
    * [<span data-ttu-id="b3e9a-125">Asymmetric1024KeyEncryptionHelper.cs</span><span class="sxs-lookup"><span data-stu-id="b3e9a-125">Asymmetric1024KeyEncryptionHelper.cs</span></span>](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/Asymmetric1024KeyEncryptionHelper.cs)
    * [<span data-ttu-id="b3e9a-126">AsymmetricHigherKeyEncryptionHelper.cs</span><span class="sxs-lookup"><span data-stu-id="b3e9a-126">AsymmetricHigherKeyEncryptionHelper.cs</span></span>](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AsymmetricHigherKeyEncryptionHelper.cs)
    * [<span data-ttu-id="b3e9a-127">AuthenticatedEncryption.cs</span><span class="sxs-lookup"><span data-stu-id="b3e9a-127">AuthenticatedEncryption.cs</span></span>](https://github.com/microsoft/PowerBI-CSharp/blob/master/sdk/PowerBI.Api/Extensions/AuthenticatedEncryption.cs) 

    ---  

5. <span data-ttu-id="b3e9a-128">สร้างรายละเอียดข้อมูลประจำตัวด้วยข้อมูลประจำตัวที่เข้ารหัสลับไว้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-128">Build credential details with encrypted credentials.</span></span>

    # <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-129">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-129">.NET SDK v3</span></span>](#tab/sdk3)

    <span data-ttu-id="b3e9a-130">ใช้คลาส AssymetricKeyEncriptor กับคีย์สาธารณะที่กู้คืนมาใน **ขั้นตอนที่ 3**</span><span class="sxs-lookup"><span data-stu-id="b3e9a-130">Use the AssymetricKeyEncryptor class with the public key retrieved in **Step 3**.</span></span>

    ```csharp
    var credentialDetails = new CredentialDetails(
            credentials,
            PrivacyLevel.Private,
            EncryptedConnection.Encrypted,
            credentialsEncryptor);
    ```


    # <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-131">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-131">.NET SDK v2</span></span>](#tab/sdk2)

    ```csharp
    var credentialDetails = new CredentialDetails(
            credentials,
            CredentialTypeEnum.Basic,
            EncryptedConnectionEnum.Encrypted,
            EncryptionAlgorithmEnum.None,
            PrivacyLevelEnum.Private);
    ```

    ---

6. <span data-ttu-id="b3e9a-132">เรียกใช้ฟังก์ชัน[แหล่งข้อมูลอัปเดต](/rest/api/power-bi/gateways/updatedatasource)เพื่อตั้งค่าข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="b3e9a-132">Call [Update Datasource](/rest/api/power-bi/gateways/updatedatasource) to set credentials.</span></span>

    ```csharp
    pbiClient.Gateways.UpdateDatasource(gatewayId, datasourceId, credentialDetails);
    ```

## <a name="configure-a-new-data-source-for-a-data-gateway"></a><span data-ttu-id="b3e9a-133">กำหนดค่าแหล่งข้อมูลใหม่สำหรับเกตเวย์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-133">Configure a new data source for a data gateway</span></span>

1. <span data-ttu-id="b3e9a-134">ติดตั้ง[เกตเวย์ข้อมูลภายในองค์กร](https://powerbi.microsoft.com/gateway/)บนเครื่องของคุณ</span><span class="sxs-lookup"><span data-stu-id="b3e9a-134">Install the [On-premises data gateway](https://powerbi.microsoft.com/gateway/) on your machine.</span></span>

2. <span data-ttu-id="b3e9a-135">เรียกใช้ฟังก์ชัน [รับเกตเวย์](/rest/api/power-bi/gateways/getgateways)เพื่อเรียกใช้คีย์สาธารณะและ ID ของเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="b3e9a-135">Call [Get Gateways](/rest/api/power-bi/gateways/getgateways) to retrieve the gateway ID and public key.</span></span>

    ```csharp
    // Select a gateway
    var gateways = pbiClient.Gateways.GetGateways().Value;
    var gateway = gateways.First();
    ```

3. <span data-ttu-id="b3e9a-136">สร้างรายละเอียดข้อมูลประจำตัวด้วยวิธีเดียวกับที่อธิบายไว้ใน [ อัปเดตโฟลว์ข้อมูลประจำตัวสำหรับแหล่งข้อมูล](#update-credentials-flow-for-data-sources) โดยใช้เกตเวย์คีย์สาธารณะที่กู้คืนมาใน **ขั้นตอนที่ 2**</span><span class="sxs-lookup"><span data-stu-id="b3e9a-136">Build credential details in the same way as described in [update credentials flow for data sources](#update-credentials-flow-for-data-sources), using the gateway public key retrieved in **step 2**.</span></span>

4. <span data-ttu-id="b3e9a-137">สร้างเนื้อความคำขอ</span><span class="sxs-lookup"><span data-stu-id="b3e9a-137">Build the request body.</span></span>

    ```csharp
    var request = new PublishDatasourceToGatewayRequest(
            dataSourceType: "SQL",
            connectionDetails: "{\"server\":\"myServer\",\"database\":\"myDatabase\"}",
            credentialDetails: credentialDetails,
            dataSourceName: "my sql datasource");
    ```

5. <span data-ttu-id="b3e9a-138">เรียกใช้ฟังก์ชัน[สร้างแหล่งข้อมูล](/rest/api/power-bi/gateways/createdatasource)API</span><span class="sxs-lookup"><span data-stu-id="b3e9a-138">Call the [Create Datasource](/rest/api/power-bi/gateways/createdatasource) API.</span></span>

    ```csharp
    pbiClient.Gateways.CreateDatasource(gateway.Id, request);
    ```

## <a name="credential-types"></a><span data-ttu-id="b3e9a-139">ชนิดข้อมูลประจำตัว</span><span class="sxs-lookup"><span data-stu-id="b3e9a-139">Credential types</span></span>

<span data-ttu-id="b3e9a-140">เมื่อคุณเรียกใช้งาน [สร้างแหล่งข้อมูล](/rest/api/power-bi/gateways/createdatasource) หรือ [อัปเดตแหล่งข้อมูล](/rest/api/power-bi/gateways/updatedatasource)ภายใต้ **เกตเวย์ภายในองค์กร** โดยใช้ [Power BI Rest API](/rest/api/power-bi/) ค่าข้อมูลประจำตัวที่จำเป็นต้องเข้ารหัสลับโดยใช้คีย์สาธารณะของเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="b3e9a-140">When you call [Create Datasource](/rest/api/power-bi/gateways/createdatasource) or [Update Datasource](/rest/api/power-bi/gateways/updatedatasource) under an **enterprise on-prem gateway** using [Power BI Rest API](/rest/api/power-bi/), the credentials value needs to be encrypted using the gateway's public key.</span></span>

>[!NOTE]
><span data-ttu-id="b3e9a-141">.NET SDK v3 ยังสามารถเรียกใช้ตัวอย่าง .NET SDK v2 ที่แสดงด้านล่างได้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-141">.NET SDK v3 can also run the .NET SDK v2 examples listed below.</span></span>

### <a name="windows-and-basic-credentials"></a><span data-ttu-id="b3e9a-142">Windows และข้อมูลประจำตัวพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="b3e9a-142">Windows and basic credentials</span></span>

# <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-143">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-143">.NET SDK v3</span></span>](#tab/sdk3)

```csharp
// Windows credentials
var credentials = new WindowsCredentials(username: "john", password: "*****");

// Or

// Basic credentials
var credentials = new BasicCredentials(username: "john", password: "*****");

var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-144">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-144">.NET SDK v2</span></span>](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"username\", \"value\":\"john\"},{\"name\":\"password\", \"value\":\"*****\"}]}";
```

---

### <a name="key-credentials"></a><span data-ttu-id="b3e9a-145">ข้อมูลประจำตัวหลัก</span><span class="sxs-lookup"><span data-stu-id="b3e9a-145">Key credentials</span></span>

# <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-146">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-146">.NET SDK v3</span></span>](#tab/sdk3)

```csharp
var credentials = new KeyCredentials("TestKey");
var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-147">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-147">.NET SDK v2</span></span>](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"key\", \"value\":\"ec....LA=\"}]}";
```

---

<span data-ttu-id="b3e9a-148">**ข้อมูลประจำตัว OAuth2**</span><span class="sxs-lookup"><span data-stu-id="b3e9a-148">**OAuth2 credentials**</span></span>

# <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-149">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-149">.NET SDK v3</span></span>](#tab/sdk3)

```csharp
var credentials = new OAuth2Credentials("TestToken");
var credentialsEncryptor = new AsymmetricKeyEncryptor(publicKey);
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.Encrypted, credentialsEncryptor);
```

# <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-150">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-150">.NET SDK v2</span></span>](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":[{\"name\":\"accessToken\", \"value\":\"eyJ0....fwtQ\"}]}";
```

---

<span data-ttu-id="b3e9a-151">**ข้อมูลประจำตัวแบบไม่ระบุชื่อ**</span><span class="sxs-lookup"><span data-stu-id="b3e9a-151">**Anonymous credentials**</span></span>

# <a name="net-sdk-v3"></a>[<span data-ttu-id="b3e9a-152">.NET SDK v3</span><span class="sxs-lookup"><span data-stu-id="b3e9a-152">.NET SDK v3</span></span>](#tab/sdk3)

```csharp
var credentials = new AnonymousCredentials();
var credentialDetails = new CredentialDetails(credentials, PrivacyLevel.Private, EncryptedConnection.NotEncrypted);
```

# <a name="net-sdk-v2"></a>[<span data-ttu-id="b3e9a-153">.NET SDK v2</span><span class="sxs-lookup"><span data-stu-id="b3e9a-153">.NET SDK v2</span></span>](#tab/sdk2)

```csharp
var credentials = "{\"credentialData\":\"\"}";
```

---

## <a name="troubleshooting"></a><span data-ttu-id="b3e9a-154">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="b3e9a-154">Troubleshooting</span></span>

### <a name="no-gateway-and-data-source-id-found-when-calling-get-data-sources"></a><span data-ttu-id="b3e9a-155">ไม่มีเกตเวย์และข้อมูล ID ที่พบเมื่อเรียกใช้ฟังก์ชันรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b3e9a-155">No gateway and data source ID found when calling get data sources</span></span>

<span data-ttu-id="b3e9a-156">ปัญหานี้หมายความว่าชุดข้อมูลไม่ได้ผูกกับเกตเวย์</span><span class="sxs-lookup"><span data-stu-id="b3e9a-156">This issue means the dataset isn't bound to a gateway.</span></span> <span data-ttu-id="b3e9a-157">เมื่อสร้างชุดข้อมูลใหม่ สำหรับการเชื่อมต่อระบบคลาวด์แต่ละระบบ แหล่งข้อมูลที่ไม่มีข้อมูลประจำตัวจะถูกสร้างขึ้นโดยอัตโนมัติบนเกตเวย์ระบบคลาวด์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b3e9a-157">When creating a new dataset, for each cloud connection a data source with no credentials is created automatically on the user's cloud gateway.</span></span> <span data-ttu-id="b3e9a-158">เกตเวย์นี้ถูกใช้เพื่อจัดเก็บข้อมูลประจำตัวสำหรับการเชื่อมต่อระบบคลาวด์</span><span class="sxs-lookup"><span data-stu-id="b3e9a-158">This gateway is used to store the credentials for cloud connections.</span></span>

<span data-ttu-id="b3e9a-159">หลังจากที่คุณสร้างชุดข้อมูล การผูกอัตโนมัติจะดำเนินการแล้วเสร็จระหว่างชุดข้อมูลและเกตเวย์ที่เหมาะสม ซึ่งประกอบด้วยแหล่งข้อมูลที่ตรงกันสำหรับการเชื่อมต่อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b3e9a-159">After you create the dataset, an automatic binding is created between the dataset and a suitable gateway, which contains matching data sources for all connections.</span></span> <span data-ttu-id="b3e9a-160">ถ้าไม่มีเกตเวย์ดังกล่าวหรือเกตเวย์ที่เหมาะสมหลายรายการ การผูกอัตโนมัติจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="b3e9a-160">If there's no such gateway or multiple suitable gateways, the automatic binding fails.</span></span>

<span data-ttu-id="b3e9a-161">หากคุณกำลังใช้ชุดข้อมูลภายในองค์กร ให้สร้างแหล่งข้อมูลในองค์กรขาดหายไปและผูกชุดข้อมูลไปยังเกตเวย์ด้วยตนเองโดยใช้ตัวเลือก[ผูกกับเกตเวย์](/rest/api/power-bi/datasets/bindtogateway)</span><span class="sxs-lookup"><span data-stu-id="b3e9a-161">If you're using on-premises datasets, create the missing on-premises data sources, and bind the dataset to a gateway manually by using [Bind To Gateway](/rest/api/power-bi/datasets/bindtogateway).</span></span>

<span data-ttu-id="b3e9a-162">หากต้องการค้นหาเกตเวย์ที่สามารถผูกได้ โปรดใช้ฟังก์ชัน[ค้นหาเกตเวย์](/rest/api/power-bi/datasets/discovergateways)</span><span class="sxs-lookup"><span data-stu-id="b3e9a-162">To discover gateways that could be bound, use [Discover Gateways](/rest/api/power-bi/datasets/discovergateways).</span></span>
