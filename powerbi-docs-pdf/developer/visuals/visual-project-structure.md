---
title: โครงสร้างของโครงการวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้อธิบายเกี่ยวกับโฟลเดอร์และโครงสร้างไฟล์ของโครงการวิชวล Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: conceptual
ms.date: 01/12/2020
ms.openlocfilehash: 4c946021138e49c0aed9668d9b3ea6079f458ccd
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888040"
---
# <a name="power-bi-visual-project-structure"></a><span data-ttu-id="6b55e-104">โครงสร้างของโครงการแสดงผล Power BI</span><span class="sxs-lookup"><span data-stu-id="6b55e-104">Power BI visual project structure</span></span>

<span data-ttu-id="6b55e-105">วิธีที่ดีที่สุดในการเริ่มต้นสร้างวิชวล Power BI ใหม่คือการใช้เครื่องมือวิชวล Power BI [.pbiviz](https://www.npmjs.com/package/powerbi-visuals-tools)</span><span class="sxs-lookup"><span data-stu-id="6b55e-105">The best way to start creating a new Power BI visual is to use the Power BI visuals [pbiviz](https://www.npmjs.com/package/powerbi-visuals-tools) tool.</span></span>

<span data-ttu-id="6b55e-106">ในการสร้างวิชวลใหม่ ให้นำทางไปยังไดเรกทอรีที่คุณต้องการให้วิชวล Power BI เข้าไปอยู่ และเรียกคำสั่งใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="6b55e-106">To create a new visual, navigate to the directory you want the Power BI visual to reside in, and run the command:</span></span>

`pbiviz new <visual project name>`

<span data-ttu-id="6b55e-107">เรียกใช้งานคำสั่งนี้สร้างโฟลเดอร์วิชวล Power BI ที่ประกอบด้วยไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6b55e-107">Running this command creates a Power BI visual folder that contains the following files:</span></span>

```markdown
project
├───.vscode
│   ├───launch.json
│   └───settings.json
├───assets
│   └───icon.png
├───node_modules
├───src
│   ├───settings.ts
│   └───visual.ts
├───style
│   └───visual.less
├───capabilities.json
├───package-lock.json
├───package.json
├───pbiviz.json
├───tsconfig.json
└───tslint.json
```

## <a name="folder-and-file-description"></a><span data-ttu-id="6b55e-108">คำอธิบายโฟลเดอร์และไฟล์</span><span class="sxs-lookup"><span data-stu-id="6b55e-108">Folder and file description</span></span>

<span data-ttu-id="6b55e-109">ส่วนนี้แสดงข้อมูลสำหรับแต่ละโฟลเดอร์และไฟล์ในไดเรกทอรีที่เครื่องมือวิชวล Power BI  **pbiviz** สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="6b55e-109">This section provides information for each folder and file in the directory that the Power BI visuals **pbiviz** tool creates.</span></span>  

### <a name="vscode"></a><span data-ttu-id="6b55e-110">.vscode</span><span class="sxs-lookup"><span data-stu-id="6b55e-110">.vscode</span></span>

<span data-ttu-id="6b55e-111">โฟลเดอร์นี้ประกอบด้วยการตั้งค่าโปรเจคโค้ด VS</span><span class="sxs-lookup"><span data-stu-id="6b55e-111">This folder contains the VS code project settings.</span></span>

<span data-ttu-id="6b55e-112">ในการกำหนดค่าพื้นที่ทำงานของคุณ แก้ไขไฟล์ `.vscode/settings.json`</span><span class="sxs-lookup"><span data-stu-id="6b55e-112">To configure your workspace, edit the `.vscode/settings.json` file.</span></span>

<span data-ttu-id="6b55e-113">สำหรับข้อมูลเพิ่มเติม ดู [การตั้งค่าผู้ใช้และพื้นที่ทำงาน](https://code.visualstudio.com/docs/getstarted/settings)</span><span class="sxs-lookup"><span data-stu-id="6b55e-113">For more information, see [User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings)</span></span>

### <a name="assets"></a><span data-ttu-id="6b55e-114">สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6b55e-114">assets</span></span>

<span data-ttu-id="6b55e-115">โฟลเดอร์นี้ประกอบด้วยไฟล์ `icon.png`</span><span class="sxs-lookup"><span data-stu-id="6b55e-115">This folder contains the `icon.png` file.</span></span>

<span data-ttu-id="6b55e-116">เครื่องมือวิชวล Power BI ใช้ไฟล์นี้เป็นไอคอนวิชวล Power BI ใหม่ ในแผงการแสดงภาพของ Power BI</span><span class="sxs-lookup"><span data-stu-id="6b55e-116">The Power BI visuals tool uses this file as the new Power BI visual icon in the Power BI visualization pane.</span></span>

### <a name="src"></a><span data-ttu-id="6b55e-117">src</span><span class="sxs-lookup"><span data-stu-id="6b55e-117">src</span></span>

<span data-ttu-id="6b55e-118">โฟลเดอร์นี้ประกอบด้วยโค้ดแหล่งที่มาของวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-118">This folder contains the visual's source code.</span></span>

<span data-ttu-id="6b55e-119">ในโฟลเดอร์นี้เครื่องมือวิชวล Power BI จะสร้างไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6b55e-119">In this folder, the Power BI visuals tool creates the following files:</span></span>
* <span data-ttu-id="6b55e-120">`visual.ts` - โค้ดแหล่งที่มาหลักของวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-120">`visual.ts` - The visual's main source code.</span></span>
* <span data-ttu-id="6b55e-121">`settings.ts` - โค้ดการตั้งค่าของวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-121">`settings.ts` - The code of the visual's settings.</span></span> <span data-ttu-id="6b55e-122">คลาสในไฟล์มีอินเทอร์เฟซสำหรับการกำหนด [คุณสมบัติของวิชวล](./objects-properties.md#properties)ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6b55e-122">The classes in the file provide an interface for defining your [visual's properties](./objects-properties.md#properties).</span></span>

### <a name="style"></a><span data-ttu-id="6b55e-123">ลักษณะ</span><span class="sxs-lookup"><span data-stu-id="6b55e-123">style</span></span>

<span data-ttu-id="6b55e-124">โฟลเดอร์นี้ประกอบด้วยไฟล์ `visual.less` ซึ่งมีลักษณะของวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-124">This folder contains the `visual.less` file, which holds the visual's styles.</span></span>

### <a name="capabilitiesjson"></a><span data-ttu-id="6b55e-125">capabilities.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-125">capabilities.json</span></span>

<span data-ttu-id="6b55e-126">ไฟล์นี้ประกอบด้วยคุณสมบัติและการตั้งค่าหลัก (หรือ [ความสามารถ](./capabilities.md)) สำหรับวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-126">This file contains the main properties and settings (or [capabilities](./capabilities.md)) for the visual.</span></span> <span data-ttu-id="6b55e-127">อนุญาตให้วิชวลทำการสนับสนุนฟีเจอร์ วัตถุ คุณสมบัติ และ [มุมมองการดูข้อมูล](./dataview-mappings.md)</span><span class="sxs-lookup"><span data-stu-id="6b55e-127">It allows the visual to declare supported features, objects, properties, and [data view mapping](./dataview-mappings.md).</span></span>

### <a name="package-lockjson"></a><span data-ttu-id="6b55e-128">package-lock.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-128">package-lock.json</span></span>

<span data-ttu-id="6b55e-129">ไฟล์นี้สร้างขึ้นมาโดยอัตโนมัติสำหรับการดำเนินการใดๆ ที่ *npm* ปรับเปลี่ยน `node_modules` แผนผังต้นไม้หรือ `package.json` ไฟล์</span><span class="sxs-lookup"><span data-stu-id="6b55e-129">This file is automatically generated for any operations where *npm* modifies either the `node_modules` tree, or the `package.json` file.</span></span>

<span data-ttu-id="6b55e-130">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไฟล์นี้ ให้ดูเอกสารกำกับโปรแกรมทางการของ [npm-package-lock.json](https://docs.npmjs.com/files/package-lock.json)</span><span class="sxs-lookup"><span data-stu-id="6b55e-130">For more information about this file, see the official [npm-package-lock.json](https://docs.npmjs.com/files/package-lock.json) documentation.</span></span>

### <a name="packagejson"></a><span data-ttu-id="6b55e-131">package.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-131">package.json</span></span>

<span data-ttu-id="6b55e-132">ไฟล์นี้อธิบายเกี่ยวกับแพคเกจโครงการ</span><span class="sxs-lookup"><span data-stu-id="6b55e-132">This file describes the project package.</span></span> <span data-ttu-id="6b55e-133">สิ่งนี้ประกอบด้วยข้อมูลเกี่ยวกับโครงการ เช่น ผู้เขียน คำอธิบายและการขึ้นต่อกันของโครงการ</span><span class="sxs-lookup"><span data-stu-id="6b55e-133">It contains information about the project such as authors, description, and project dependencies.</span></span>

<span data-ttu-id="6b55e-134">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับไฟล์นี้ ให้ดูเอกสารกำกับโปรแกรมทางการของ [npm-package-lock.json](https://docs.npmjs.com/files/package.json.html)</span><span class="sxs-lookup"><span data-stu-id="6b55e-134">For more information about this file, see the official [npm-package.json](https://docs.npmjs.com/files/package.json.html) documentation.</span></span>

### <a name="pbivizjson"></a><span data-ttu-id="6b55e-135">pbiviz.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-135">pbiviz.json</span></span>

<span data-ttu-id="6b55e-136">ไฟล์นี้ประกอบด้วยเมตาดาต้าวิชวล</span><span class="sxs-lookup"><span data-stu-id="6b55e-136">This file contains the visual metadata.</span></span>

<span data-ttu-id="6b55e-137">ในการดูตัวอย่าง `pbiviz.json` ไฟล์ที่มีข้อคิดเห็นที่อธิบายรายการเมตาดาต้า ให้ดูที่ส่วน[รายการเมตาดาต้า](#metadata-entries)</span><span class="sxs-lookup"><span data-stu-id="6b55e-137">To view an example `pbiviz.json` file with comments describing the metadata entries, see the [metadata entries](#metadata-entries) section.</span></span>

### <a name="tsconfigjson"></a><span data-ttu-id="6b55e-138">tsconfig.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-138">tsconfig.json</span></span>

<span data-ttu-id="6b55e-139">ไฟล์การกำหนดค่าสำหรับ [TypeScript](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html).</span><span class="sxs-lookup"><span data-stu-id="6b55e-139">A configuration file for [TypeScript](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html).</span></span>

<span data-ttu-id="6b55e-140">ไฟล์นี้ต้องประกอบด้วยเส้นทางไปยังแฟ้ม **\*.ts** ที่มีชั้นหลักของวิชวลตั้งอยู่ ที่ระบุเฉพาะใน `visualClassName` คุณสมบัติใน `pbiviz.json` ไฟล์</span><span class="sxs-lookup"><span data-stu-id="6b55e-140">This file must contain the path to **\*.ts** file where the main class of the visual is located, as specified in the `visualClassName` property in the `pbiviz.json` file.</span></span>

### <a name="tslintjson"></a><span data-ttu-id="6b55e-141">tslint.json</span><span class="sxs-lookup"><span data-stu-id="6b55e-141">tslint.json</span></span>

<span data-ttu-id="6b55e-142">ไฟล์นี้ประกอบด้วย [การกำหนดค่า TSLint](https://palantir.github.io/tslint/usage/configuration/)</span><span class="sxs-lookup"><span data-stu-id="6b55e-142">This file contains the [TSLint configuration](https://palantir.github.io/tslint/usage/configuration/).</span></span>

## <a name="metadata-entries"></a><span data-ttu-id="6b55e-143">รายการเมตาดาต้า</span><span class="sxs-lookup"><span data-stu-id="6b55e-143">Metadata entries</span></span>

<span data-ttu-id="6b55e-144">ข้อคิดเห็นในคำบรรยายโค้ดต่อไปนี้จากไฟล์ `pbiviz.json`ที่อธิบายรายการเมตาดาต้า</span><span class="sxs-lookup"><span data-stu-id="6b55e-144">The comments in the following code caption from the `pbiviz.json` file, describe the metadata entries.</span></span>

> [!NOTE]
> * <span data-ttu-id="6b55e-145">จากเวอร์ชัน 3.x.x ของเครื่องมือ **pbiviz** `externalJS` ไม่ได้รับการรองรับ</span><span class="sxs-lookup"><span data-stu-id="6b55e-145">From version 3.x.x of the **pbiviz** tool,`externalJS` isn't supported.</span></span>
> * <span data-ttu-id="6b55e-146">การสนับสนุนตามท้องถิ่น [ให้เพิ่ม Power BI ที่ระบุวิชวลของคุณ](./localization.md)</span><span class="sxs-lookup"><span data-stu-id="6b55e-146">For localization support, [add the Power BI locale to your visual](./localization.md).</span></span>

```json
{
  "visual": {
     // The visual's internal name.
    "name": "<visual project name>",

    // The visual's display name.
    "displayName": "<visual project name>",

    // The visual's unique ID.
    "guid": "<visual project name>23D8B823CF134D3AA7CC0A5D63B20B7F",

    // The name of the visual's main class. Power BI creates the instance of this class to start using the visual in a Power BI report.
    "visualClassName": "Visual",

    // The visual's version number.
    "version": "1.0.0",
    
    // The visual's description (optional)
    "description": "",

    // A URL linking to the visual's support page (optional).
    "supportUrl": "",

    // A link to the source code available from GitHub (optional).
    "gitHubUrl": ""
  },
  // The version of the Power BI API the visual is using.
  "apiVersion": "2.6.0",

  // The name of the visual's author and email.
  "author": { "name": "", "email": "" },

  // 'icon' holds the path to the icon file in the assets folder; the visual's display icon.
  "assets": { "icon": "assets/icon.png" },

  // Contains the paths for JS libraries used in the visual.
  // Note: externalJS' isn't used in the Power BI visuals tool version 3.x.x or higher.
  "externalJS": null,

  // The path to the 'visual.less' style file.
  "style": "style/visual.less",

  // The path to the `capabilities.json` file.
  "capabilities": "capabilities.json",

  // The path to the `dependencies.json` file which contains information about R packages used in R based visuals.
  "dependencies": null,

  // An array of paths to files with localizations.
  "stringResources": []
}
```

## <a name="next-steps"></a><span data-ttu-id="6b55e-147">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="6b55e-147">Next steps</span></span>

* <span data-ttu-id="6b55e-148">ในการเข้าใจการโต้ตอบระหว่างวิชวล ผู้ใช้และ Power BI ดู [แนวคิดวิชวลของ Power BI](./power-bi-visuals-concept.md)</span><span class="sxs-lookup"><span data-stu-id="6b55e-148">To understand the interactions between a visual, a user, and Power BI, see [Power BI visual concept](./power-bi-visuals-concept.md).</span></span>

* <span data-ttu-id="6b55e-149">เริ่มต้นการพัฒนาวิชวล Power BI ของคุณเองตั้งแต่เริ่มต้น โดยใช้ [ด้วยคำแนะนำทีละขั้นตอน](./develop-circle-card.md)</span><span class="sxs-lookup"><span data-stu-id="6b55e-149">Start developing your own Power BI visuals from scratch, using the [step by step guide](./develop-circle-card.md).</span></span>
