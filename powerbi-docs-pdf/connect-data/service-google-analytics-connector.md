---
title: 'บริการจากบุคคลที่สาม: ตัวเชื่อมต่อ Google Analytics'
description: 'บริการจากบุคคลที่สาม: ตัวเชื่อมต่อ Google Analytics สำหรับ Power BI Desktop'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.custom: seodec18
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 05/08/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: 383f69bd371e4b0f635ff2b64c7fae0523c360e4
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96392277"
---
# <a name="use-the-google-analytics-connector-for-power-bi-desktop"></a><span data-ttu-id="f936c-103">ใช้ตัวเชื่อมต่อ Google Analytics สำหรับ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="f936c-103">Use the Google Analytics connector for Power BI Desktop</span></span>
> [!NOTE]
> <span data-ttu-id="f936c-104">ชุดเนื้อหา Google Analytics และตัวเชื่อมต่อใน Power BI Desktop พึ่งพา Google Analytics Core Reporting API</span><span class="sxs-lookup"><span data-stu-id="f936c-104">The Google Analytics content pack and the connector in Power BI Desktop rely on the Google Analytics Core Reporting API.</span></span> <span data-ttu-id="f936c-105">ด้วยเหตุนี้ คุณลักษณะและความพร้อมใช้งาน อาจแตกต่างกันไปตามเวลา</span><span class="sxs-lookup"><span data-stu-id="f936c-105">As such, features and availability may vary over time.</span></span>

<span data-ttu-id="f936c-106">คุณสามารถเชื่อมต่อกับข้อมูล Google Analytics โดยใช้ตัวเชื่อมต่อ **Google Analytics** ได้</span><span class="sxs-lookup"><span data-stu-id="f936c-106">You can connect to Google Analytics data using the **Google Analytics** connector.</span></span> <span data-ttu-id="f936c-107">เพื่อเชื่อมต่อ ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f936c-107">To connect, follow these steps:</span></span>

1. <span data-ttu-id="f936c-108">ใน **Power BI Desktop** เลือก **รับข้อมูล** จากการแท็บ ribbon **หน้าแรก**</span><span class="sxs-lookup"><span data-stu-id="f936c-108">In **Power BI Desktop**, select **Get Data** from the **Home** ribbon tab.</span></span>
2. <span data-ttu-id="f936c-109">ในหน้าต่าง **รับข้อมูล** เลือก **บริการออนไลน์** จากประเภทในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="f936c-109">In the **Get Data** window, select **Online Services** from the categories in the left pane.</span></span>
3. <span data-ttu-id="f936c-110">เลือก **Google Analytics** จากตัวเลือกในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="f936c-110">Select **Google Analytics** from the selections in the right pane.</span></span>
4. <span data-ttu-id="f936c-111">ที่ด้านล่างของหน้าต่าง เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="f936c-111">At the bottom of the window, select **Connect**.</span></span>  
   <span data-ttu-id="f936c-112">![หน้าจอของแท็บหน้าแรก ที่แสดงแถบเครื่องมือริบบอนรับข้อมูลพร้อมด้วย Google Analytics ที่เลือกไว้และปุ่มเชื่อมต่อ](media/service-google-analytics-connector/tps_googleanalytics_1.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-112">![Screenshot of the Home tab, showing the Get Data ribbon with Google Analytics selected and Connect button.](media/service-google-analytics-connector/tps_googleanalytics_1.png)</span></span>

<span data-ttu-id="f936c-113">คุณได้รับพร้อมท์กล่องโต้ตอบที่อธิบายว่า ตัวเชื่อมต่อเป็นบริการจากบุคคลที่สาม และเตือนเกี่ยวกับคุณลักษณะและความพร้อมใช้งาน ที่อาจเปลี่ยนไปตามช่วงเวลา และคำอธิบายอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="f936c-113">You're prompted with a dialog that explains that the connector is a Third-Party Service, and warns about how features and availability may change over time, and other clarifications.</span></span>  
![ภาพหน้าจอของกล่องโต้ตอบการเชื่อมต่อ ที่แสดงคำเตือนว่าตัวเชื่อมต่อทำงานโดยใช้บริการของบุคคลที่สาม](media/service-google-analytics-connector/tps_googleanalytics_2.png)

<span data-ttu-id="f936c-115">เมื่อคุณเลือก **ดำเนินการต่อ** คุณจะได้รับพร้อมท์ให้ลงชื่อเข้าใช้ Google Analytics</span><span class="sxs-lookup"><span data-stu-id="f936c-115">When you select **Continue**, you're prompted to sign in to Google Analytics.</span></span>  
<span data-ttu-id="f936c-116">![ภาพหน้าจอของข้อความแจ้งเตือน Google Analytics ที่แสดงว่าคุณจำเป็นต้องลงชื่อเข้าใช้เพื่อเชื่อมต่อ](media/service-google-analytics-connector/tps_googleanalytics_3.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-116">![Screenshot of the Google Analytics prompt, showing that you need to sign in to connect.](media/service-google-analytics-connector/tps_googleanalytics_3.png)</span></span>

<span data-ttu-id="f936c-117">เมื่อคุณใส่ข้อมูลประจำตัวของคุณ คุณได้รับพร้อมท์ว่า Power BI ต้องสามารถเข้าถึงแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="f936c-117">When you enter your credentials, you're prompted that Power BI would like to have offline access.</span></span> <span data-ttu-id="f936c-118">นี่คือวิธีที่คุณใช้ **Power BI Desktop** เพื่อเข้าถึงข้อมูล Google Analytics ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f936c-118">This is how you use **Power BI Desktop** to access your Google Analytics data.</span></span>  

<span data-ttu-id="f936c-119">เมื่อคุณยอมรับ **Power BI Desktop** แสดงให้เห็นว่าคุณลงชื่อเข้าใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="f936c-119">Once you accept, **Power BI Desktop** shows that you're currently signed in.</span></span>  
<span data-ttu-id="f936c-120">![ภาพหน้าจอของข้อความแจ้งเตือน Google Analytics ที่แสดงว่าคุณลงชื่อเข้าใช้](media/service-google-analytics-connector/tps_googleanalytics_5.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-120">![Screenshot of the Google Analytics prompt, showing that you are signed in.](media/service-google-analytics-connector/tps_googleanalytics_5.png)</span></span>

<span data-ttu-id="f936c-121">เลือก **เชื่อมต่อ** และข้อมูล Google Analytics ของคุณ จะถูกเชื่อมต่อกับ **Power BI Desktop** และโหลดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f936c-121">Select **Connect**, and your Google Analytics data is connected to **Power BI Desktop**, and loads the data.</span></span>  
<span data-ttu-id="f936c-122">![ภาพหน้าจอของกล่องโต้ตอบโหลด ที่แสดงว่ามีการเชื่อมต่อและโหลดข้อมูล Google Analytics](media/service-google-analytics-connector/tps_googleanalytics_6.png)</span><span class="sxs-lookup"><span data-stu-id="f936c-122">![Screenshot of the Load dialog, showing the Google Analytics data is connected and loading.](media/service-google-analytics-connector/tps_googleanalytics_6.png)</span></span>

## <a name="changes-to-the-api"></a><span data-ttu-id="f936c-123">การเปลี่ยนแปลงของ API</span><span class="sxs-lookup"><span data-stu-id="f936c-123">Changes to the API</span></span>
<span data-ttu-id="f936c-124">แม้ว่าเราพยายามเผยแพร่อัปเดตที่สอดคล้องกับการเปลี่ยนแปลงใด ๆ API อาจเปลี่ยนแปลงในลักษณะที่ส่งผลกระทบต่อผลลัพธ์ของคิวรีที่เราสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f936c-124">Although we attempt to release updates in accordance with any changes, the API may change in a way that affects the results of the queries we generate.</span></span> <span data-ttu-id="f936c-125">ในบางกรณี บางแบบสอบถามอาจไม่สนับสนุนอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="f936c-125">In some cases, certain queries may no longer be supported.</span></span> <span data-ttu-id="f936c-126">เนื่องจากการต้องพึ่งพาจากบุคคลที่สามนี้ เราไม่สามารถรับประกันผลลัพธ์ของคิวรีคุณเมื่อใช้ตัวเชื่อมต่อนี้</span><span class="sxs-lookup"><span data-stu-id="f936c-126">Due to this dependency we cannot guarantee the results of your queries when using this connector.</span></span>

<span data-ttu-id="f936c-127">รายละเอียดเพิ่มเติมเกี่ยวกับ การเปลี่ยนแปลง Google Analytics API สามารถอ่านใน[บันทึกการเปลี่ยนแปลง](https://developers.google.com/analytics/devguides/changelog)ของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="f936c-127">More details on changes to the Google Analytics API can be found in their [changelog](https://developers.google.com/analytics/devguides/changelog).</span></span>

