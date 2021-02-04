---
title: สร้างใบรับรอง SSL สำหรับวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีการสร้างใบรับรอง SSL โดยใช้เครื่องมือวิชวล Power BI ใน Windows, Mac หรือ Linux หรือด้วยตนเอง เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 05/08/2020
ms.openlocfilehash: 7897d25f3ac49c0f1b728f2aaf05b8612de67055
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97885533"
---
# <a name="create-an-ssl-certificate"></a><span data-ttu-id="c9689-104">สร้างใบรับรอง SSL</span><span class="sxs-lookup"><span data-stu-id="c9689-104">Create an SSL certificate</span></span>

<span data-ttu-id="c9689-105">บทความนี้อธิบายวิธีการสร้างและติดตั้งใบรับรอง Secure Sockets Layer (SSL) สำหรับวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="c9689-105">This article describes how to generate and install Secure Sockets Layer (SSL) certificates for Power BI visuals.</span></span>

<span data-ttu-id="c9689-106">สำหรับกระบวนการ Windows, macOS X และ Linux คุณต้องมีเครื่องมือวิชวล Power BI **pbiviz** แพคเกจที่ติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="c9689-106">For the Windows, macOS X, and Linux procedures, you must have the Power BI Visual Tools **pbiviz** package installed.</span></span> <span data-ttu-id="c9689-107">สำหรับข้อมูลเพิ่มเติม ดู [การตั้งค่าสภาพแวดล้อมของคุณสําหรับการพัฒนาวิชวล Power BI](./environment-setup.md)</span><span class="sxs-lookup"><span data-stu-id="c9689-107">For more information, see [Set up your environment for developing a Power BI visual](./environment-setup.md).</span></span> 

## <a name="create-a-certificate-on-windows"></a><span data-ttu-id="c9689-108">สร้างใบรับรองบน Windows</span><span class="sxs-lookup"><span data-stu-id="c9689-108">Create a certificate on Windows</span></span>

<span data-ttu-id="c9689-109">หากต้องการสร้างใบรับรองโดยใช้ PowerShell `New-SelfSignedCertificate` cmdlet บน Windows 8 และใหม่กว่า ให้เรียกใช้คำสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-109">To generate a certificate by using the PowerShell cmdlet `New-SelfSignedCertificate` on Windows 8 and later, run the following command:</span></span>

```powershell
pbiviz --install-cert
```

<span data-ttu-id="c9689-110">สำหรับ Windows 7  `pbiviz` เครื่องมือจำเป็นต้องใช้โปรแกรมอรรถประโยชน์ OpenSSL เพื่อให้มีใช้จากบรรทัดคำสั่ง</span><span class="sxs-lookup"><span data-stu-id="c9689-110">For Windows 7, the `pbiviz` tool requires the OpenSSL utility to be available from the command line.</span></span> <span data-ttu-id="c9689-111">หากต้องการติดตั้ง OpenSSL ให้ไปที่ [OpenSSL](https://www.openssl.org) หรือ [OpenSSL Binaries](https://wiki.openssl.org/index.php/Binaries)</span><span class="sxs-lookup"><span data-stu-id="c9689-111">To install OpenSSL, go to [OpenSSL](https://www.openssl.org) or [OpenSSL Binaries](https://wiki.openssl.org/index.php/Binaries).</span></span>

<span data-ttu-id="c9689-112">สำหรับข้อมูลเพิ่มเติมและคำแนะนำสำหรับการติดตั้งใบรับรอง ดู [สร้างและติดตั้งใบรับรองสำหรับ Windows](./environment-setup.md#create-and-install-a-certificate)</span><span class="sxs-lookup"><span data-stu-id="c9689-112">For more information and instructions for installing a certificate, see [Create and install a certificate for Windows](./environment-setup.md#create-and-install-a-certificate).</span></span>

## <a name="create-a-certificate-on-macos-x"></a><span data-ttu-id="c9689-113">สร้างใบรับรองบน macOS X</span><span class="sxs-lookup"><span data-stu-id="c9689-113">Create a certificate on macOS X</span></span>

<span data-ttu-id="c9689-114">โปรแกรมอรรถประโยชน์ OpenSSL มักจะพร้อมใช้งานในระบบปฏิบัติการ macOS X</span><span class="sxs-lookup"><span data-stu-id="c9689-114">The OpenSSL utility is usually available in the macOS X operating system.</span></span>

<span data-ttu-id="c9689-115">คุณยังสามารถติดตั้งโปรแกรมอรรถประโยชน์ OpenSSL โดยการเรียกใช้คำสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-115">You can also install the OpenSSL utility by running either of the following commands:</span></span>

- <span data-ttu-id="c9689-116">จากตัวจัดการแพ็คเกจ *Brew*</span><span class="sxs-lookup"><span data-stu-id="c9689-116">From the *Brew* package manager:</span></span>
  
  ```cmd
  brew install openssl
  brew link openssl --force
  ```

- <span data-ttu-id="c9689-117">โดยใช้ *MacPorts*:</span><span class="sxs-lookup"><span data-stu-id="c9689-117">By using *MacPorts*:</span></span>
  
  ```cmd
  sudo port install openssl
  ```

<span data-ttu-id="c9689-118">หลังจากที่คุณติดตั้งโปรแกรมอรรถประโยชน์ OpenSSL ให้เรียกใช้คำสั่งต่อไปนี้เพื่อสร้างใบรับรองใหม่:</span><span class="sxs-lookup"><span data-stu-id="c9689-118">After you install the OpenSSL utility, run the following command to generate a new certificate:</span></span>

```cmd
pbiviz --install-cert
```

<span data-ttu-id="c9689-119">สำหรับข้อมูลเพิ่มเติมและคำแนะนำให้ดูแท็บ OSX ใน [สร้างและติดตั้งใบรับรอง](./environment-setup.md#create-and-install-a-certificate)</span><span class="sxs-lookup"><span data-stu-id="c9689-119">For more information and instructions, see the OSX tab in [Create and install a certificate](./environment-setup.md#create-and-install-a-certificate).</span></span>

## <a name="create-a-certificate-on-linux"></a><span data-ttu-id="c9689-120">สร้างใบรับรองบน Linux</span><span class="sxs-lookup"><span data-stu-id="c9689-120">Create a certificate on Linux</span></span>

<span data-ttu-id="c9689-121">โปรแกรมอรรถประโยชน์ OpenSSL มักจะพร้อมใช้งานในระบบปฏิบัติการ Linux</span><span class="sxs-lookup"><span data-stu-id="c9689-121">The OpenSSL utility is usually available in the Linux operating system.</span></span>

<span data-ttu-id="c9689-122">ก่อนที่คุณจะเริ่มต้นให้เรียกใช้คำสั่งต่อไปนี้เพื่อตรวจสอบให้แน่ใจว่ามีการติดตั้ง `openssl` และ `certutil`:</span><span class="sxs-lookup"><span data-stu-id="c9689-122">Before you begin, run the following commands to make sure `openssl` and `certutil` are installed:</span></span>

```sh
which openssl
which certutil
```

<span data-ttu-id="c9689-123">หากไม่ได้ติดตั้ง `openssl` และ `certutil` ให้ติดตั้งโปรแกรมอรรถประโยชน์ `openssl` และ `libnss3`</span><span class="sxs-lookup"><span data-stu-id="c9689-123">If `openssl` and `certutil` aren't installed, install the `openssl` and `libnss3` utilities.</span></span>

### <a name="create-the-ssl-configuration-file"></a><span data-ttu-id="c9689-124">สร้างไฟล์การกำหนดค่า SSL</span><span class="sxs-lookup"><span data-stu-id="c9689-124">Create the SSL configuration file</span></span>

<span data-ttu-id="c9689-125">สร้างไฟล์ชื่อ */tmp/openssl.cnf* ที่มีข้อความต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-125">Create a file called */tmp/openssl.cnf* that contains the following text:</span></span>

```
authorityKeyIdentifier=keyid,issuer
basicConstraints=CA:FALSE
keyUsage = digitalSignature, nonRepudiation, keyEncipherment, dataEncipherment
subjectAltName = @alt_names

[ alt_names ]
DNS.1=localhost
```

### <a name="generate-root-certificate-authority"></a><span data-ttu-id="c9689-126">สร้างผู้ออกใบรับรองหลัก</span><span class="sxs-lookup"><span data-stu-id="c9689-126">Generate root certificate authority</span></span>

<span data-ttu-id="c9689-127">ในการสร้างผู้ออกใบรับรองหลัก (CA) ในการลงชื่อใบรับรองในเครื่องให้เรียกใช้คำสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-127">To generate root certificate authority (CA) to sign local certificates, run the following commands:</span></span>

```sh
touch $HOME/.rnd
openssl req -x509 -nodes -new -sha256 -days 1024 -newkey rsa:2048 -keyout /tmp/local-root-ca.key -out /tmp/local-root-ca.pem -subj "/C=US/CN=Local Root CA/O=Local Root CA"
openssl x509 -outform pem -in /tmp/local-root-ca.pem -out /tmp/local-root-ca.crt
```

### <a name="generate-a-certificate-for-localhost"></a><span data-ttu-id="c9689-128">สร้างใบรับรองสำหรับ localhost</span><span class="sxs-lookup"><span data-stu-id="c9689-128">Generate a certificate for localhost</span></span> 

<span data-ttu-id="c9689-129">หากต้องการสร้างใบรับรองสำหรับ `localhost` โดยใช้ *CA และ* openssl ที่สร้างขึ้นให้เรียกใช้คำสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-129">To generate a certificate for `localhost` using the generated CA and *openssl.cnf*, run the following commands:</span></span>

```sh
PBIVIZ=`which pbiviz`
PBIVIZ=`dirname $PBIVIZ`
PBIVIZ="$PBIVIZ/../lib/node_modules/powerbi-visuals-tools/certs"
# Make sure that $PBIVIZ contains the correct certificate directory path. ls $PBIVIZ should list 'blank' file.
openssl req -new -nodes -newkey rsa:2048 -keyout $PBIVIZ/PowerBIVisualTest_private.key -out $PBIVIZ/PowerBIVisualTest.csr -subj "/C=US/O=PowerBI Visuals/CN=localhost"
openssl x509 -req -sha256 -days 1024 -in $PBIVIZ/PowerBIVisualTest.csr -CA /tmp/local-root-ca.pem -CAkey /tmp/local-root-ca.key -CAcreateserial -extfile /tmp/openssl.cnf -out $PBIVIZ/PowerBIVisualTest_public.crt
```

### <a name="add-root-certificates"></a><span data-ttu-id="c9689-130">เพิ่มใบรับรองหลัก</span><span class="sxs-lookup"><span data-stu-id="c9689-130">Add root certificates</span></span>

<span data-ttu-id="c9689-131">หากต้องการเพิ่มใบรับรองหลักลงในฐานข้อมูลของเบราว์เซอร์ Chrome ให้เรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="c9689-131">To add a root certificate to the Chrome browser's database, run:</span></span>

```sh
certutil -A -n "Local Root CA" -t "CT,C,C" -i /tmp/local-root-ca.pem -d sql:$HOME/.pki/nssdb
```

<span data-ttu-id="c9689-132">หากต้องการเพิ่มใบรับรองหลักลงในฐานข้อมูลของเบราว์เซอร์ Mozilla Firefox ให้เรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="c9689-132">To add a root certificate to the Mozilla Firefox browser's database, run:</span></span>

```sh
for certDB in $(find $HOME/.mozilla* -name "cert*.db")
do
certDir=$(dirname ${certDB});
certutil -A -n "Local Root CA" -t "CT,C,C" -i /tmp/local-root-ca.pem -d sql:${certDir}
done
```

<span data-ttu-id="c9689-133">เมื่อต้องการเพิ่มใบรับรองหลักทั้งระบบ ให้เรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="c9689-133">To add a system-wide root certificate, run:</span></span>

```sh
sudo cp /tmp/local-root-ca.pem /usr/local/share/ca-certificates/
sudo update-ca-certificates
```

### <a name="remove-root-certificates"></a><span data-ttu-id="c9689-134">เอาใบรับรองหลักออก</span><span class="sxs-lookup"><span data-stu-id="c9689-134">Remove root certificates</span></span>

<span data-ttu-id="c9689-135">เมื่อต้องการเอาใบรับรองหลักออก ให้เรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="c9689-135">To remove a root certificate, run:</span></span>

```sh
sudo rm /usr/local/share/ca-certificates/local-root-ca.pem
sudo update-ca-certificates --fresh
```

## <a name="generate-a-certificate-manually"></a><span data-ttu-id="c9689-136">สร้างใบรับรองด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c9689-136">Generate a certificate manually</span></span>

<span data-ttu-id="c9689-137">คุณยังสามารถสร้างใบรับรอง SSL ด้วยตนเองโดยใช้ OpenSSL</span><span class="sxs-lookup"><span data-stu-id="c9689-137">You can also generate an SSL certificate manually using OpenSSL.</span></span> <span data-ttu-id="c9689-138">คุณสามารถระบุเครื่องมือใดๆ ในการสร้างใบรับรองของคุณ</span><span class="sxs-lookup"><span data-stu-id="c9689-138">You can specify any tools to generate your certificates.</span></span>

<span data-ttu-id="c9689-139">ถ้ามีการติดตั้งโปรแกรมอรรถประโยชน์ OpenSSL อยู่แล้วให้สร้างใบรับรองใหม่โดยการเรียกใช้:</span><span class="sxs-lookup"><span data-stu-id="c9689-139">If the OpenSSL utility is already installed, generate a new certificate by running:</span></span>

```cmd
openssl req -x509 -newkey rsa:4096 -keyout PowerBIVisualTest_private.key -out PowerBIVisualTest_public.crt -days 365
```

<span data-ttu-id="c9689-140">โดยปกติแล้วคุณสามารถค้นหาใบรับรองเว็บเซิร์ฟเวอร์ `PowerBI-visuals-tools` ได้โดยการเรียกใช้คำสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-140">You can usually find the `PowerBI-visuals-tools` web server certificates by running one of the following commands:</span></span>

- <span data-ttu-id="c9689-141">สำหรับอินสแตนซ์ส่วนกลางของเครื่องมือ:</span><span class="sxs-lookup"><span data-stu-id="c9689-141">For the global instance of the tools:</span></span>
  
  ```cmd
  %appdata%\npm\node_modules\PowerBI-visuals-tools\certs
  ```

- <span data-ttu-id="c9689-142">สำหรับอินสแตนซ์เฉพาะที่ของเครื่องมือ:</span><span class="sxs-lookup"><span data-stu-id="c9689-142">For the local instance of the tools:</span></span>
  
  ```cmd
  <Power BI visual project root>\node_modules\PowerBI-visuals-tools\certs
  ```

### <a name="pem-format"></a><span data-ttu-id="c9689-143">รูปแบบ PEM</span><span class="sxs-lookup"><span data-stu-id="c9689-143">PEM format</span></span>

<span data-ttu-id="c9689-144">ถ้าคุณใช้รูปแบบใบรับรอง Privacy Enhanced Mail (PEM) บันทึกไฟล์ใบรับรองเป็น *PowerBIVisualTest_public.crt* และบันทึกคีย์ส่วนตัวเป็น *PowerBIVisualTest_private.key*</span><span class="sxs-lookup"><span data-stu-id="c9689-144">If you use the Privacy Enhanced Mail (PEM) certificate format, save the certificate file as *PowerBIVisualTest_public.crt*, and save the private key as *PowerBIVisualTest_private.key*.</span></span>

### <a name="pfx-format"></a><span data-ttu-id="c9689-145">รูปแบบ PFX</span><span class="sxs-lookup"><span data-stu-id="c9689-145">PFX format</span></span>

<span data-ttu-id="c9689-146">ถ้าคุณใช้รูปแบบใบรับรอง Personal Information Exchange (PFX) บันทึกไฟล์ใบรับรองเป็น *PowerBIVisualTest_public.pfx*</span><span class="sxs-lookup"><span data-stu-id="c9689-146">If you use the Personal Information Exchange (PFX) certificate format, save the certificate file as *PowerBIVisualTest_public.pfx*.</span></span>

<span data-ttu-id="c9689-147">หากไฟล์ใบรับรอง PFX ของคุณต้องการวลีรหัสผ่านให้ทำดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c9689-147">If your PFX certificate file requires a passphrase:</span></span>

1. <span data-ttu-id="c9689-148">ในไฟล์กำหนดค่า ให้ระบุว่า:</span><span class="sxs-lookup"><span data-stu-id="c9689-148">In the config file, specify:</span></span>
   
   ```cmd
   \PowerBI-visuals-tools\config.json
   ```
   
1. <span data-ttu-id="c9689-149">ในส่วน `server`ระบุข้อความรหัสผ่านโดยแทนที่ \<YOUR PASSPHRASE> ตัวแทนข้อความ:</span><span class="sxs-lookup"><span data-stu-id="c9689-149">In the `server` section, specify the passphrase by replacing the \<YOUR PASSPHRASE> placeholder:</span></span>

    ```cmd
    "server":{
        "root":"webRoot",
        "assetsRoute":"/assets",
        "privateKey":"certs/PowerBIVisualTest_private.key",
        "certificate":"certs/PowerBIVisualTest_public.crt",
        "pfx":"certs/PowerBIVisualTest_public.pfx",
        "port":"8080",
        "passphrase":"<YOUR PASSPHRASE>"
    }
    ```

## <a name="next-steps"></a><span data-ttu-id="c9689-150">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="c9689-150">Next steps</span></span>
- [<span data-ttu-id="c9689-151">พัฒนาวิชวล BI การ์ดวงกลม Power</span><span class="sxs-lookup"><span data-stu-id="c9689-151">Develop a Power circle card BI visual</span></span>](develop-circle-card.md)
- [<span data-ttu-id="c9689-152">ตัวอย่างวิชวล Power BI</span><span class="sxs-lookup"><span data-stu-id="c9689-152">Power BI visuals samples</span></span>](samples.md)
- [<span data-ttu-id="c9689-153">เผยแพร่วิชวล Power BI ลงใน AppSource</span><span class="sxs-lookup"><span data-stu-id="c9689-153">Publish a Power BI visual to AppSource</span></span>](office-store.md)